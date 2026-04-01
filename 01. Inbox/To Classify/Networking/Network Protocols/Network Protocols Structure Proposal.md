
# Network Protocols Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Network Protocols` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Network Protocols
    ├── Link Layer Protocols
    ├── Network Layer Protocols
    │   └── Routing Protocols
    ├── Transport Layer Protocols
    └── Application Layer Protocols
        └── HTTP
            ├── HTTP Messages
            ├── HTTP Methods
            ├── HTTP Status Codes
            ├── HTTP Header Fields
            └── HTTP Versions
```

## Почему структура именно такая

- `Network Protocols` уже оправдан как `sub-overview`, потому что тема естественно распадается на устойчивые protocol families, а не на одну статью с бесконечным перечислением.
- Организация по слоям лучше, чем случайный список протокольных имен, потому что она сразу связывает протокол с его функциональной ролью в сетевом стеке.
- `Network Layer Protocols` оправданы как отдельная overview-ветка, потому что внутри них естественно возникает дополнительный подкласс `Routing Protocols`.
- `Routing Protocols` лучше держать вложенной веткой, а не смешивать с любыми network-layer protocols, поскольку это особая группа control protocols про выбор маршрутов и распространение маршрутной информации.
- `HTTP` уже оправдан как отдельная application-layer ветка, потому что у него есть собственный устойчивый корпус аспектов и внутренняя структура.
- Остальные конкретные протоколы вроде `TCP`, `UDP`, `IP` и `BGP` пока не стоит выносить в отдельные notes без соседнего корпуса и примеров сравнения.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Network Protocols` внутрь `Internet`, потому что понятие протокола шире современной Internet-ветки.
- Не стоит создавать длинный плоский список отдельных protocols под `Networking`.
- Не стоит дублировать ту же иерархию отдельно под `OSI Model` и `TCP IP Model`, если здесь уже есть общая protocol-ветка.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `HTTP` нужны `DNS`, `SMTP` и `DHCP` как отдельные подветки
- [ ] Решить, когда нужны отдельные notes про `TCP`, `UDP`, `IP` и `ICMP`
- [ ] Проверить, нужен ли отдельный узел про `Protocol Encapsulation`
- [ ] Проверить `related`
