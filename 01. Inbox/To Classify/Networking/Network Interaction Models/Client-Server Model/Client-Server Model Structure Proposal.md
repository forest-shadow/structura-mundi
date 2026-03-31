# Client-Server Model Structure Proposal

## Краткое определение

Предлагаемое место для `Client-Server Model` внутри ветки `Networking` как отдельного model-centric `sub-overview`.

## Рекомендуемая иерархия

```text
Networking
└── Network Interaction Models
    └── Client-Server Model
        ├── Client
        └── Server
            ├── Server Application
            ├── Server Process
            ├── Server Host
            └── Service Endpoint
```

## Почему структура именно такая

- `Client-Server Model` задает первичную логическую рамку взаимодействия и естественно живет внутри более общей ветки `Network Interaction Models`.
- `Server` нужно делать `overview`, потому что это явно многослойный термин, а не одна простая article-note.
- `Server Process` следует выделять отдельно, потому что operational server engineering быстро образует самостоятельный кластер.

## Что не стоит делать прямо сейчас

- Не стоит определять `Server` только как машину или только как процесс.
- Не стоит смешивать `Service Endpoint` с самим сервером.
- Не стоит переносить эту ветку в `Operating Systems`, потому что первичный смысл здесь сетевой и архитектурный.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Load Balancing`, `Backpressure` и `Service Discovery`
- [ ] Проверить будущие `related` со смежными distributed-systems notes
