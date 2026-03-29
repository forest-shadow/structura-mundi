
Предлагаемое устройство domain-root ветки `Networking` внутри `Computer Science`.

## Рекомендуемая иерархия

```text
Computer Science
└── Networking
    ├── Network Topology
    │   ├── Physical and Logical Network Topology
    │   └── Common Network Topologies
    │       ├── Point-to-Point Network Topology
    │       ├── Bus Network Topology
    │       ├── Star Network Topology
    │       ├── Ring Network Topology
    │       ├── Mesh Network Topology
    │       ├── Tree Network Topology
    │       └── Hybrid Network Topology
    ├── Network Performance
    │   ├── Network Bandwidth
    │   ├── Network Throughput
    │   ├── Network Latency
    │   ├── Network Jitter
    │   └── Network Packet Loss
    ├── Network Protocols
    │   ├── Link Layer Protocols
    │   ├── Network Layer Protocols
    │   │   └── Routing Protocols
    │   ├── Transport Layer Protocols
    │   └── Application Layer Protocols
    ├── Internet
    │   ├── TCP IP Model
    │   │   ├── TCP IP Link Layer
    │   │   ├── TCP IP Internet Layer
    │   │   ├── TCP IP Transport Layer
    │   │   └── TCP IP Application Layer
    │   ├── IP Addressing
    │   ├── Routing
    │   └── DNS
    │       ├── DNS Resolution
    │       ├── Recursive Resolver
    │       ├── Authoritative DNS Server
    │       ├── DNS Resource Record
    │       └── DNS Zone
    └── OSI Model
        ├── Physical Layer
        ├── Data Link Layer
        ├── Network Layer
        ├── Transport Layer
        ├── Session Layer
        ├── Presentation Layer
        └── Application Layer
```

## Почему структура именно такая

- `Networking` оправдан как domain-root overview, потому что внутри него уже есть как минимум несколько самостоятельных обзорных веток: structural topology branch, performance-metrics branch, protocol-families branch, operational Internet branch и model-centric OSI branch.
- `Network Topology` лучше держать отдельным `sub-overview` прямо под `Networking`, потому что это общая structural тема о формах организации сетей, а не часть только Internet или только OSI.
- `Common Network Topologies` лучше делать вложенной overview-веткой внутри `Network Topology`, чтобы не плодить длинный плоский список однотипных topology patterns на верхнем уровне.
- `Network Performance` лучше держать отдельным `sub-overview` под `Networking`, потому что bandwidth, throughput, latency, jitter и loss образуют устойчивый кластер cross-cutting metrics, а не частный раздел одной Internet-ветки.
- `Network Protocols` лучше держать отдельным `sub-overview` под `Networking`, потому что protocol families образуют самостоятельную понятийную ветку, которую не стоит растворять ни в `Internet`, ни в `OSI Model`.
- `Internet` стоит делать отдельным `sub-overview`, потому что это не один isolated concept, а устойчивый кластер вокруг TCP/IP, адресации, маршрутизации и naming.
- `DNS` внутри `Internet` уже лучше делать не одиночной статьей, а отдельным `sub-overview`, потому что тема естественно распадается на resolution, server roles и data model.
- `OSI Model` лучше держать sibling-веткой, а не child-узлом `Internet`, потому что это концептуальная модель сетевых функций, а не часть самой Internet topology.

## Что не стоит делать прямо сейчас

- Не стоит плодить отдельный `overview` только ради симметрии между всеми возможными networking subfields.
- Не стоит заранее выносить каждый отдельный протокол в самостоятельную note без плотного корпуса.
- Не стоит помещать `Network Topology` под `Internet`, потому что это сделает слишком узкой более общую networking-тему.
- Не стоит помещать `Network Bandwidth` как одиночную статью прямо под `Networking`, потому что без throughput, latency и loss она плохо удерживает собственные границы.
- Не стоит превращать `Network Protocols` сразу в свалку notes про `TCP`, `UDP`, `HTTP`, `BGP` и `DNS` без промежуточных family-overviews.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужен `Network Architecture`
- [ ] Решить, когда рядом нужен `Network Congestion`
- [ ] Решить, когда `Network Protocols` пора дробить на concrete protocol notes
- [ ] Проверить `related`

# Networking: Рекомендуемый маршрут чтения

1. Начать с `[[Network Topology]]`, если нужен язык для описания формы и связности сети.
2. Затем перейти к `[[Network Performance]]`, если нужен язык для описания capacity и качества доставки.
3. Затем перейти к `[[Network Protocols]]`, если нужен общий язык для описания protocol families.
4. После этого читать `[[Internet]]`, если нужен operational взгляд на современную сеть.
5. Затем перейти к `[[TCP IP Model]]` и связанным статьям внутри Internet-ветки.
6. Затем сопоставить это с `[[OSI Model]]` как с соседней концептуальной моделью.


# Internet: Рекомендуемый маршрут чтения

1. Начать с `[[TCP IP Model]]`, чтобы зафиксировать стек Internet protocol suite.
2. Затем перейти к `[[IP Addressing]]`.
3. После этого читать `[[Routing]]`.
4. Завершить `[[DNS]]` как слой distributed naming поверх сетевой адресации.
