# Go Servers Structure Proposal

## Краткое определение

Предлагаемое место для `Go Servers` внутри ветки `Go` как language-specific server-engineering `sub-overview`.

## Рекомендуемая иерархия

```text
Go
└── Go Servers
    ├── HTTP Server in Go
    ├── gRPC Server in Go
    ├── TCP Server in Go
    ├── Go Server Concurrency
    ├── Go Server Lifecycle
    ├── Timeouts and Cancellation in Go Servers
    ├── Observability in Go Servers
    │   └── related: Go pprof
    └── Resource Management in Go Servers
```

## Почему структура именно такая

- Ветка должна жить внутри `Go`, а не внутри общей заметки `Server`, потому что это language-specific operational практика.
- Здесь сервер уже рассматривается не как абстрактная роль, а как приложение или процесс, работающий с listener, goroutines, contexts и lifecycle.
- Отдельные protocol-shaped notes полезны, потому что HTTP, gRPC и custom TCP servers в Go имеют общую server-side рамку, но разные operational контуры.
- `Go pprof` не стоит делать дочерним узлом `Go Servers`, потому что pprof применим не только к серверам; правильнее держать его в `Go Runtime Diagnostics` и связывать с `Observability in Go Servers` через `related`.

## Что не стоит делать прямо сейчас

- Не стоит смешивать `Go Servers` с общей `Go Concurrency Model`: concurrency здесь должна обсуждаться как server workload concern, а не как вся модель языка.
- Не стоит превращать `Go Servers` в плоский каталог фреймворков и библиотек.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Middleware in Go Servers` и `Dependency Wiring for Go Servers`
- [ ] Проверить будущие `related` с `Telemetry`, `Go pprof` и `Connection Pooling`
