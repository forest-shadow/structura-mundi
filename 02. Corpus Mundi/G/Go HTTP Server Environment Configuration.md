---
aliases:
  - Go HTTP Server ENV Config
  - Go Server Production Environment Configuration
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Servers]]"
status: draft
related:
  - "[[Go Servers]]"
  - "[[HTTP Server in Go]]"
  - "[[Go Server Lifecycle]]"
  - "[[Timeouts and Cancellation in Go Servers]]"
  - "[[Observability in Go Servers]]"
  - "[[Go pprof]]"
  - "[[Resource Management in Go Servers]]"
tags: []
---
# 1. Go HTTP Server Environment Configuration

> <font color="#fb4934">Production-ready environment configuration for a Go HTTP server</font> — это внешняя параметризация HTTP-процесса на Go, которая задаёт его сетевую границу, timeouts, resource limits, lifecycle-поведение, security posture, observability-сигналы и параметры downstream-зависимостей без пересборки бинаря.

В зрелой инженерной практике `.env` или иная env-конфигурация не считается «просто списком строк». Она выступает operational contract между кодом, инфраструктурой, оркестратором, reverse proxy, SRE-процедурами и политиками безопасности. Хорошая env-модель нужна не ради удобства, а для того, чтобы сервис в production вёл себя предсказуемо под нагрузкой, при деградации зависимостей, при rolling deploy и при инцидентах.

# 2. Production-ready baseline `.env`

```dotenv
# Service identity
APP_NAME=payments-api
APP_ENV=production
APP_VERSION=1.4.3
APP_INSTANCE_ID=
APP_REGION=eu-central-1

# Go runtime
GOMAXPROCS=0
GOMEMLIMIT=1536MiB

# Main HTTP listener
HTTP_HOST=0.0.0.0
HTTP_PORT=8080
HTTP_BASE_URL=https://api.example.com
HTTP_READ_TIMEOUT=15s
HTTP_READ_HEADER_TIMEOUT=5s
HTTP_WRITE_TIMEOUT=30s
HTTP_IDLE_TIMEOUT=120s
HTTP_MAX_HEADER_BYTES=1048576
HTTP_MAX_BODY_BYTES=10485760

# Backpressure and protection
HTTP_MAX_CONNS=20000
HTTP_CONCURRENCY_LIMIT=2000
HTTP_RATE_LIMIT_RPS=0
HTTP_RATE_LIMIT_BURST=0

# Lifecycle and deploy behavior
SERVER_STARTUP_TIMEOUT=30s
SERVER_READY_TIMEOUT=10s
SERVER_DRAIN_TIMEOUT=20s
SERVER_GRACEFUL_SHUTDOWN_TIMEOUT=30s

# Reverse proxy and client IP trust
HTTP_TRUST_PROXY_HEADERS=true
HTTP_TRUSTED_PROXY_CIDRS=10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
HTTP_REAL_IP_HEADER=X-Forwarded-For

# TLS
HTTP_TLS_ENABLED=false
HTTP_TLS_CERT_FILE=
HTTP_TLS_KEY_FILE=
HTTP_TLS_MIN_VERSION=1.2
HTTP_TLS_CLIENT_AUTH_MODE=none

# Security headers and browser-facing policy
HTTP_HSTS_ENABLED=true
HTTP_HSTS_MAX_AGE=31536000
HTTP_HSTS_INCLUDE_SUBDOMAINS=true
HTTP_HSTS_PRELOAD=false
HTTP_CORS_ALLOWED_ORIGINS=https://app.example.com
HTTP_CORS_ALLOWED_METHODS=GET,POST,PUT,PATCH,DELETE,OPTIONS
HTTP_CORS_ALLOWED_HEADERS=Authorization,Content-Type,Idempotency-Key,X-Request-ID
HTTP_CORS_EXPOSED_HEADERS=X-Request-ID
HTTP_CORS_ALLOW_CREDENTIALS=false

# Logging
LOG_LEVEL=info
LOG_FORMAT=json
LOG_ADD_SOURCE=false
LOG_SAMPLING_ENABLED=false

# Health, metrics, profiling, tracing
HEALTH_PATH=/healthz
READINESS_PATH=/readyz
METRICS_ENABLED=true
METRICS_PATH=/metrics
ADMIN_BIND_ADDR=127.0.0.1:9000
PPROF_ENABLED=false
OTEL_ENABLED=true
OTEL_SERVICE_NAME=payments-api
OTEL_EXPORTER_OTLP_ENDPOINT=otel-collector.monitoring.svc.cluster.local:4317
OTEL_EXPORTER_OTLP_INSECURE=true
OTEL_TRACE_SAMPLING_RATIO=0.10

# Outbound HTTP client defaults
OUTBOUND_HTTP_TIMEOUT=10s
OUTBOUND_HTTP_DIAL_TIMEOUT=3s
OUTBOUND_HTTP_TLS_HANDSHAKE_TIMEOUT=3s
OUTBOUND_HTTP_RESPONSE_HEADER_TIMEOUT=5s
OUTBOUND_HTTP_IDLE_CONN_TIMEOUT=90s
OUTBOUND_HTTP_MAX_IDLE_CONNS=200
OUTBOUND_HTTP_MAX_IDLE_CONNS_PER_HOST=50
OUTBOUND_HTTP_MAX_CONNS_PER_HOST=100

# Optional stateful dependencies
DATABASE_DSN=
DATABASE_MAX_OPEN_CONNS=50
DATABASE_MAX_IDLE_CONNS=25
DATABASE_CONN_MAX_LIFETIME=30m
REDIS_ADDR=
REDIS_PASSWORD=
REDIS_DIAL_TIMEOUT=1s
REDIS_READ_TIMEOUT=500ms
REDIS_WRITE_TIMEOUT=500ms
```

# 3. Почему группы переменных вообще нужны

Production-конфигурация удобнее всего мыслится не как плоский набор ключей, а как набор слоёв ответственности:
- **Identity and runtime**: кто мы, в какой среде живём, сколько CPU и памяти можем съесть.
- **Listener and request budget**: где слушаем, сколько читаем, сколько пишем и когда рвём слишком медленные соединения.
- **Lifecycle**: как стартуем, когда считаем себя готовыми, сколько времени даём на draining и graceful shutdown.
- **Trust and security**: где заканчивается TLS, каким proxy доверяем, какие браузерные политики выставляем.
- **Observability**: какие сигналы отдаём наружу во время нормальной работы и во время расследования инцидента.
- **Downstream control**: как ограничиваем исходящие вызовы, чтобы не умереть от собственных зависимостей.

Если эти группы не выделить отдельно, конфигурация быстро превращается в хаотический список флагов, в котором невозможно понять, какая переменная решает проблему безопасности, какая — проблему latency, а какая — проблему завершения деплоя.

# 4. Service identity and Go runtime

Эти переменные описывают идентичность процесса и ограничивают поведение Go runtime.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `APP_NAME` | Имя сервиса в логах, метриках, tracing и service discovery. | Устраняет путаницу между сервисами в observability-стеке. |
| `APP_ENV` | Фиксирует среду исполнения: `local`, `dev`, `stage`, `production`. | Не даёт случайно включить dev-поведение в production или наоборот. |
| `APP_VERSION` | Версия сборки или Git SHA. | Позволяет быстро связать регрессию с конкретным релизом. |
| `APP_INSTANCE_ID` | Идентификатор конкретного pod/VM/process instance. | Упрощает корреляцию инцидентов на уровне отдельного экземпляра. |
| `APP_REGION` | Регион, зона или локация развёртывания. | Помогает расследовать региональные деградации и асимметрию latency. |
| `GOMAXPROCS` | Верхняя граница числа одновременно работающих OS threads для Go scheduler. Значение `0` обычно означает автонастройку. | Предотвращает неэффективное использование CPU и конфликт с cgroup limits. |
| `GOMEMLIMIT` | Верхний memory budget для Go runtime. | Снижает риск OOMKill и runaway memory growth под нагрузкой. |

Практический смысл этой группы в том, что сервис должен знать не только «что он делает», но и «в какой среде он это делает» и «какой ресурсный коридор ему выделен».

# 5. Main HTTP listener and request budget

Это ядро HTTP-сервера: адрес прослушивания, timeouts и лимиты на протокольном уровне.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `HTTP_HOST` | Сетевой интерфейс bind. Обычно `0.0.0.0` в контейнере. | Явно задаёт network boundary и предотвращает случайный bind не на тот интерфейс. |
| `HTTP_PORT` | Порт входящего HTTP listener. | Делает сервис переносимым между средами и оркестраторами. |
| `HTTP_BASE_URL` | Канонический внешний URL сервиса. | Нужен для корректной генерации callback URLs, redirects и self-links. |
| `HTTP_READ_TIMEOUT` | Общее время на чтение запроса. | Ограничивает hanging clients и защищает от медленных соединений. |
| `HTTP_READ_HEADER_TIMEOUT` | Время на чтение только заголовков. | Явно снижает риск Slowloris-атак. |
| `HTTP_WRITE_TIMEOUT` | Максимальное время на запись ответа. | Не даёт воркерам бесконечно висеть на медленном клиенте. |
| `HTTP_IDLE_TIMEOUT` | Время жизни keep-alive idle connection. | Контролирует расход file descriptors и socket pressure. |
| `HTTP_MAX_HEADER_BYTES` | Максимальный объём HTTP-заголовков. | Защищает память и парсер от oversized headers. |
| `HTTP_MAX_BODY_BYTES` | Максимальный размер request body. | Предотвращает memory blow-up и неожиданно дорогие загрузки. |

Эти переменные создают bounded transport layer. Без них сервер остаётся функциональным, но перестаёт быть production-safe.

# 6. Backpressure and overload protection

Эта группа не про «ускорение сервера», а про контролируемую деградацию под перегрузкой.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `HTTP_MAX_CONNS` | Глобальный предел одновременно открытых входящих соединений. | Предотвращает исчерпание file descriptors и memory per connection. |
| `HTTP_CONCURRENCY_LIMIT` | Максимум одновременно исполняемых handler-операций. | Не даёт server-side fan-out уничтожить CPU, heap и downstream-пулы. |
| `HTTP_RATE_LIMIT_RPS` | Лимит запросов в секунду. `0` обычно означает отключено. | Ограничивает abuse, burst storms и неравномерный всплеск трафика. |
| `HTTP_RATE_LIMIT_BURST` | Допустимый кратковременный burst поверх базового RPS. | Сохраняет эластичность без перехода в неконтролируемую перегрузку. |

Эта группа нужна потому, что Go очень дешёво создаёт goroutines, но downstream-системы, heap и TCP stack не бесконечны.

# 7. Lifecycle and deploy behavior

Эти переменные делают сервер совместимым с rolling deploy, drain-процедурами и graceful shutdown.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `SERVER_STARTUP_TIMEOUT` | Верхняя граница на инициализацию listeners, telemetry и зависимостей. | Не даёт процессу бесконечно зависнуть на старте. |
| `SERVER_READY_TIMEOUT` | Время, после которого сервис либо становится ready, либо считается проблемным. | Помогает orchestration layer быстро отсекать плохие инстансы. |
| `SERVER_DRAIN_TIMEOUT` | Время между выключением readiness и окончательным stop serving. | Даёт load balancer время перестать слать новый трафик. |
| `SERVER_GRACEFUL_SHUTDOWN_TIMEOUT` | Максимум времени на завершение in-flight запросов и cleanup. | Предотвращает внезапный kill активных операций при деплое или рестарте. |

Эта группа решает одну из самых частых production-проблем: сервис работает нормально в steady-state, но ломается именно в момент деплоя, рестарта или node eviction.

# 8. Reverse proxy trust and client identity

Если сервис стоит за NGINX, Envoy, ingress-controller или cloud load balancer, ему нужно явно понимать, каким proxy можно доверять.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `HTTP_TRUST_PROXY_HEADERS` | Включает использование `X-Forwarded-*` или аналогичных заголовков. | Делает корректными scheme, host и client IP за reverse proxy. |
| `HTTP_TRUSTED_PROXY_CIDRS` | Список доверенных proxy-сетей. | Защищает от spoofing клиентского IP через поддельные forwarded headers. |
| `HTTP_REAL_IP_HEADER` | Имя заголовка, из которого извлекается исходный IP. | Убирает неоднозначность при работе с разными proxy-цепочками. |

Без этой группы логирование IP, rate limiting, geo-analysis и audit trail часто оказываются ложными.

# 9. TLS and transport security

TLS-переменные определяют, где заканчивается шифрование и насколько строгим должен быть transport security policy.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `HTTP_TLS_ENABLED` | Включает встроенный TLS на уровне самого Go-сервера. | Позволяет явно различать edge TLS и TLS termination на proxy. |
| `HTTP_TLS_CERT_FILE` | Путь к сертификату сервера. | Нужен для локальной termination или internal-only TLS. |
| `HTTP_TLS_KEY_FILE` | Путь к приватному ключу. | Делает возможным запуск HTTPS без пересборки бинаря. |
| `HTTP_TLS_MIN_VERSION` | Минимальная версия TLS, например `1.2` или `1.3`. | Запрещает старые и небезопасные протоколы. |
| `HTTP_TLS_CLIENT_AUTH_MODE` | Режим клиентской аутентификации: `none`, `require`, `verify-if-given` и т. п. | Поддерживает mTLS-сценарии и zero-trust perimeter. |

Важно: если TLS уже терминируется на ingress, эти переменные всё равно полезны, потому что позволяют явно зафиксировать архитектурное решение, а не оставлять его неявным.

# 10. Browser-facing security headers and CORS

Эта группа актуальна для API, которые вызываются браузером или участвуют в web flows.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `HTTP_HSTS_ENABLED` | Включает заголовок Strict-Transport-Security. | Снижает риск downgrade на HTTP после первого HTTPS-захода. |
| `HTTP_HSTS_MAX_AGE` | Время жизни HSTS policy в секундах. | Делает политику транспорта устойчивой на стороне браузера. |
| `HTTP_HSTS_INCLUDE_SUBDOMAINS` | Распространяет HSTS на поддомены. | Предотвращает слабое звено в поддоменах общей зоны. |
| `HTTP_HSTS_PRELOAD` | Помечает намерение на preload-list. | Помогает enforce-ить HTTPS ещё до первого визита пользователя. |
| `HTTP_CORS_ALLOWED_ORIGINS` | Белый список источников, которым разрешён браузерный доступ. | Не даёт случайно открыть API всему интернету. |
| `HTTP_CORS_ALLOWED_METHODS` | Разрешённые HTTP-методы для cross-origin запросов. | Ограничивает поверхность атаки и лишние preflight-сценарии. |
| `HTTP_CORS_ALLOWED_HEADERS` | Разрешённые входящие заголовки в CORS. | Делает preflight-поведение предсказуемым. |
| `HTTP_CORS_EXPOSED_HEADERS` | Заголовки, которые браузер может прочитать из ответа. | Позволяет явно отдать нужные correlation IDs и metadata. |
| `HTTP_CORS_ALLOW_CREDENTIALS` | Разрешает ли cookies или credentials в cross-origin запросах. | Предотвращает опасные конфигурации, несовместимые с wildcard origins. |

Большая часть CORS-инцидентов возникает не из-за отсутствия CORS, а из-за слишком широких настроек, которые сначала удобны, а потом становятся security debt.

# 11. Logging, health, metrics, profiling, tracing

Это operational nervous system сервиса.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `LOG_LEVEL` | Минимальный уровень логов: `debug`, `info`, `warn`, `error`. | Позволяет менять подробность диагностики без пересборки сервиса. |
| `LOG_FORMAT` | Формат логов, обычно `json`. | Делает логи пригодными для машинного разбора и агрегации. |
| `LOG_ADD_SOURCE` | Добавляет файл и строку вызова в лог. | Помогает при сложной отладке, но может удорожать логи. |
| `LOG_SAMPLING_ENABLED` | Включает sampling для повторяющихся логов. | Защищает logging pipeline и бюджет хранения в штормах ошибок. |
| `HEALTH_PATH` | Endpoint liveness или health. | Даёт оркестратору и мониторингу единый способ проверить, что процесс жив. |
| `READINESS_PATH` | Endpoint readiness. | Позволяет корректно исключать инстанс из трафика во время старта и draining. |
| `METRICS_ENABLED` | Включает экспорт метрик. | Делает возможным latency, error и saturation analysis. |
| `METRICS_PATH` | Путь для scrape метрик. | Упрощает интеграцию с Prometheus и агентами мониторинга. |
| `ADMIN_BIND_ADDR` | Отдельный bind-адрес для admin endpoints. | Изолирует sensitive operational endpoints от публичного listener. |
| `PPROF_ENABLED` | Включает `[[Go pprof]]`. | Даёт инструменты для CPU, heap и goroutine-диагностики в сложных инцидентах. |
| `OTEL_ENABLED` | Включает экспорт tracing-сигналов. | Делает видимым путь запроса через сервис и зависимости. |
| `OTEL_SERVICE_NAME` | Имя сервиса для OpenTelemetry. | Обеспечивает консистентную идентификацию в trace backend. |
| `OTEL_EXPORTER_OTLP_ENDPOINT` | Адрес OTLP collector/exporter. | Внешне задаёт маршрут отправки телеметрии. |
| `OTEL_EXPORTER_OTLP_INSECURE` | Режим insecure transport для OTLP, если это оправдано внутренней сетью. | Явно фиксирует transport assumptions observability pipeline. |
| `OTEL_TRACE_SAMPLING_RATIO` | Доля сэмплируемых trace, например `0.10`. | Позволяет балансировать глубину диагностики и стоимость telemetry. |

Наблюдаемость — это не «приятный бонус». В production она заменяет возможность заглянуть внутрь процесса руками.

# 12. Outbound HTTP client defaults

Многие Go HTTP-сервисы погибают не на входящем трафике, а на исходящих вызовах к зависимостям.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `OUTBOUND_HTTP_TIMEOUT` | Общий timeout исходящего HTTP-запроса. | Не даёт зависнуть на медленном downstream навсегда. |
| `OUTBOUND_HTTP_DIAL_TIMEOUT` | Timeout установления TCP-соединения. | Быстро обрывает попытки достучаться до недоступной сети или хоста. |
| `OUTBOUND_HTTP_TLS_HANDSHAKE_TIMEOUT` | Timeout на TLS handshake. | Предотвращает зависание на проблемной криптографии или сетевой деградации. |
| `OUTBOUND_HTTP_RESPONSE_HEADER_TIMEOUT` | Время ожидания заголовков ответа. | Ограничивает slow downstream, который принял запрос, но не отвечает. |
| `OUTBOUND_HTTP_IDLE_CONN_TIMEOUT` | Время жизни idle keep-alive соединений. | Контролирует reuse соединений и расход сокетов. |
| `OUTBOUND_HTTP_MAX_IDLE_CONNS` | Глобальный предел idle connections в пуле. | Не даёт пулу бесконтрольно разрастись. |
| `OUTBOUND_HTTP_MAX_IDLE_CONNS_PER_HOST` | Лимит idle connections на хост. | Балансирует reuse и fairness по downstream-узлам. |
| `OUTBOUND_HTTP_MAX_CONNS_PER_HOST` | Общий предел соединений на хост. | Защищает и сам сервис, и downstream от connection storm. |

Если эти параметры не вынесены наружу, любой всплеск latency в зависимости превращается в каскадную деградацию всего сервиса.

# 13. Optional stateful dependencies

Это уже не чисто HTTP-слой, а типичные инфраструктурные адаптеры, которые у большинства production-сервисов всё равно есть.

| Переменная | Для чего используется | Какую проблему решает |
| --- | --- | --- |
| `DATABASE_DSN` | Строка подключения к основной БД. | Отделяет бинарь от конкретной инфраструктуры и секрета подключения. |
| `DATABASE_MAX_OPEN_CONNS` | Верхняя граница открытых DB connections. | Предотвращает перегрузку БД и connection storms. |
| `DATABASE_MAX_IDLE_CONNS` | Число idle соединений в пуле. | Снижает цену частых reconnect при умеренной нагрузке. |
| `DATABASE_CONN_MAX_LIFETIME` | Максимальная продолжительность жизни одного соединения. | Помогает избежать деградации из-за long-lived stale connections. |
| `REDIS_ADDR` | Адрес Redis. | Делает topology зависимости внешней по отношению к коду. |
| `REDIS_PASSWORD` | Пароль или секрет Redis. | Устраняет хардкод чувствительных данных. |
| `REDIS_DIAL_TIMEOUT` | Timeout подключения к Redis. | Быстро обнаруживает недоступность узла. |
| `REDIS_READ_TIMEOUT` | Timeout чтения ответа Redis. | Ограничивает latency при перегрузке или сетевой деградации. |
| `REDIS_WRITE_TIMEOUT` | Timeout записи команд в Redis. | Предотвращает зависание клиентского пула на медленном сокете. |

Эта группа особенно важна потому, что именно connection pools и timeouts к stateful dependency чаще всего становятся реальным bottleneck сервиса.

# 14. Практические правила использования

- Не смешивать env-переменные уровня процесса и бизнес-флаги предметной области в один бесформенный список.
- Не использовать «магические» timeout-значения без budget thinking: входящий timeout должен быть согласован с timeouts downstream-вызовов и общим request deadline.
- Не включать `[[Go pprof]]` и admin endpoints на публичном listener.
- Не доверять `X-Forwarded-For` без списка доверенных proxy CIDR.
- Не оставлять `HTTP_MAX_BODY_BYTES`, `HTTP_MAX_HEADER_BYTES` и connection limits неограниченными.
- Не включать слишком подробный tracing или debug logging без оценки стоимости и шума.
- Не считать, что `http.ListenAndServe()` с дефолтами уже достаточно для production.

# 15. Минимальный production baseline, если нужна компактная версия

Если нужно не «всё», а действительно минимальный безопасный набор, то почти всегда обязательны:
- `APP_NAME`
- `APP_ENV`
- `HTTP_HOST`
- `HTTP_PORT`
- `HTTP_READ_HEADER_TIMEOUT`
- `HTTP_READ_TIMEOUT`
- `HTTP_WRITE_TIMEOUT`
- `HTTP_IDLE_TIMEOUT`
- `HTTP_MAX_HEADER_BYTES`
- `HTTP_MAX_BODY_BYTES`
- `SERVER_DRAIN_TIMEOUT`
- `SERVER_GRACEFUL_SHUTDOWN_TIMEOUT`
- `LOG_LEVEL`
- `LOG_FORMAT`
- `HEALTH_PATH`
- `READINESS_PATH`
- `METRICS_ENABLED`
- `OUTBOUND_HTTP_TIMEOUT`
- `OUTBOUND_HTTP_MAX_CONNS_PER_HOST`

Именно этот набор уже переводит сервис из состояния «работает у меня локально» в состояние «его можно более-менее безопасно запускать под реальной нагрузкой».

# 16. Связи с другими заметками

Родительская тема:
- `[[Go Servers]]`

Связанные заметки:
- `[[HTTP Server in Go]]`
- `[[Go Server Lifecycle]]`
- `[[Timeouts and Cancellation in Go Servers]]`
- `[[Observability in Go Servers]]`
- `[[Go pprof]]`
- `[[Resource Management in Go Servers]]`
