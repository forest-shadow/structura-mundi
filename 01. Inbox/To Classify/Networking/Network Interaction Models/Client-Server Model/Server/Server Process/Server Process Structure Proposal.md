# Server Process Structure Proposal

## Краткое определение

Предлагаемое место для `Server Process` как operational sub-overview внутри ветки `Server`.

## Рекомендуемая иерархия

```text
Server
└── Server Process
    ├── Network Listener
    ├── Request Handling
    ├── Server Concurrency Model
    ├── Server Lifecycle Management
    ├── Timeouts and Cancellation
    ├── Server Observability
    └── Server Resource Management
```

## Почему структура именно такая

- `Server Process` в инженерной практике слишком широк для одной статьи: здесь смешиваются networking, concurrency, lifecycle и runtime behavior.
- Ветку полезно строить вокруг operational concerns, а не вокруг конкретного протокола.
- Эта структура одинаково применима к HTTP, gRPC и custom TCP servers, поэтому остается достаточно общей.

## Что не стоит делать прямо сейчас

- Не стоит дробить ветку по языкам программирования; language-specific реализация должна жить отдельно, например в `Go`.
- Не стоит делать отдельные узлы под каждый системный вызов вроде `bind` или `accept`, пока нет корпуса соседних notes.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Connection Lifecycle`, `Backpressure` и `Load Shedding`
- [ ] Проверить будущие `related` с `Operating Systems` и `Distributed Systems`
