---
aliases:
  - Connection Pooling Branch Structure Proposal
note_type: article
area: computer-science
domain: software-architecture
section: architecture-patterns
parent:
status: draft
related:
  - "[[Connection Pooling]]"
  - "[[Database Connection Pooling]]"
  - "[[Databases]]"
tags: []
---

# Connection Pooling Structure Proposal

## Краткое определение

Этот файл фиксирует корректное место для двух сходных, но не сводимых друг к другу заметок:

- `[[Connection Pooling]]`
- `[[Database Connection Pooling]]`

По правилам `Principia Rerum` между ними должна быть поперечная содержательная связь через `related`, а не родительство в одном дереве.

## Выбранная оптика

- `Connection Pooling`
  - `area: computer-science`
  - `domain: software-architecture`
  - `section: architecture-patterns`
  - `parent: [[Software Architecture]]`
- `Database Connection Pooling`
  - `area: computer-science`
  - `domain: databases`
  - `section: database-connections`
  - `parent: [[Databases]]`

## Почему структура именно такая

- `Connection Pooling` отвечает на вопрос о пуле соединений как об общем инженерном паттерне повторного использования дорогого ресурса.
- `Database Connection Pooling` отвечает уже на другой вопрос: как этот паттерн ведет себя именно в контексте СУБД, серверных лимитов, transaction behavior и saturation.
- `Database Connection Pooling` не должен быть дочерней статьей `Connection Pooling`, потому что database-specific материал не является просто частным абзацем общей статьи, а образует собственную прикладную перспективу внутри domain `databases`.
- `Connection Pooling` не должен переезжать в `databases`, потому что тема шире БД и нужна для разговора о client pools, proxies, middleware и других connection-oriented системах.

## Рекомендуемая иерархия

```text
Software Architecture
└── Connection Pooling

Databases
└── Database Connection Pooling
```

Поперечная связь:

```text
Connection Pooling ↔ Database Connection Pooling
```

## Что раскрывает каждая заметка

- `Connection Pooling`: что такое пул соединений как общий паттерн, зачем он нужен, какие trade-offs вводит, чем отличается от простого connection reuse, где применяется помимо БД.
- `Database Connection Pooling`: server-side session cost, connection budget, saturation, влияние размера пула на latency и throughput, long-running transactions, lock waits, параметры `max_open_conns`, `max_idle_conns`, `lifetime`, `idle timeout`, взаимодействие с DB proxy и PgBouncer.

## Что не стоит делать

- делать `Database Connection Pooling` дочерней статьей `Connection Pooling`;
- смешивать общие pooling trade-offs с database-specific operational tuning в одной канонической заметке;
- вводить отдельные тематические template-файлы: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда в database-ветке нужен отдельный обзорный узел `Database Connections`
- [ ] Проверить, когда рядом нужны `DB Proxy` и `PgBouncer`
- [ ] Проверить `related`
