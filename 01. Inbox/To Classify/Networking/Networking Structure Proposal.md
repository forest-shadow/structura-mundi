# Networking Structure Proposal

## Назначение

Этот файл фиксирует рабочую иерархию domain-root ветки `Networking` внутри `Computer Science` по правилам `Principia Rerum`.

Словарная рамка для рабочей ветки:

- `domain: networking`
- `section: network-topology`
- `section: network-performance`
- `section: network-protocols`
- `section: network-security`
- `section: internet`
- `section: dns`
- `section: network-models`
- `section: packet-switches`

## Рекомендуемая иерархия

```text
Computer Science
└── Networking
    ├── Client-Server Model
    │   ├── Client
    │   └── Server
    │       ├── Server Application
    │       ├── Server Process
    │       │   ├── Network Listener
    │       │   ├── Request Handling
    │       │   ├── Server Concurrency Model
    │       │   ├── Server Lifecycle Management
    │       │   ├── Timeouts and Cancellation
    │       │   ├── Server Observability
    │       │   └── Server Resource Management
    │       ├── Server Host
    │       └── Service Endpoint
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
    ├── Network Security
    │   └── VPN
    │       ├── Remote Access VPN
    │       ├── Site-to-Site VPN
    │       ├── VPN Tunneling
    │       └── VPN Protocol Families
    ├── Packet Switches
    │   ├── Router
    │   └── Link-Layer Switch
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

- `Networking` оправдан как domain-root overview, потому что внутри него уже есть несколько устойчивых обзорных веток с разной оптикой.
- `Client-Server Model` уместно держать как отдельный `sub-overview`, потому что здесь нужен именно model-centric язык для ролей взаимодействия, не сводимый ни к transport protocols, ни к host infrastructure.
- `Server` лучше оформлять как `overview`, а не как одну перегруженную `article`, потому что термин одновременно живет на уровне роли, программного компонента, процесса, хоста и сетевой точки входа.
- `Server Process` тоже оправдан как вложенный `overview`, потому что вокруг него уже возникает устойчивый operational cluster: listener, request handling, concurrency, lifecycle, timeouts, observability и resource management.
- `Packet Switches` лучше держать отдельной sibling-веткой рядом с `Network Protocols` и `Internet`, потому что устройства пересылки пакетов и кадров образуют собственный понятийный кластер.
- `Network Security` оправдана как отдельная sibling-ветка рядом с `Network Protocols` и `Internet`, потому что защищенный сетевой доступ, туннелирование и trust boundaries образуют собственный понятийный кластер.
- `VPN` уже лучше оформлять как `sub-overview`, а не как одиночный article, потому что внутри темы быстро возникают разные deployment patterns, tunnel mechanics и protocol families.
- `Router` и `Link-Layer Switch` логично собирать под `Packet Switches`, а не разносить по разным моделям стека, потому что здесь важнее их общая роль forwarding devices.
- `Network Protocols` лучше не смешивать с `Packet Switches`: протоколы описывают правила взаимодействия, а switches и routers являются устройствами, реализующими пересылку и коммутацию.
- `VPN` не стоит прятать напрямую под `Internet` или `Network Protocols`, потому что тема VPN описывает не только протокол, но и security pattern защищенного логического канала поверх недоверенной сети.
- `Internet` остаётся отдельной operational-веткой про современную сетевую среду, где routing и addressing рассматриваются как рабочие механизмы реального интернета.
- `OSI Model` и `TCP IP Model` остаются model-centric ветками, а не контейнерами для всех device notes.

## Что не стоит делать прямо сейчас

- не создавать отдельные тематические template-файлы под Networking или Packet Switches, потому что по `Principia Rerum` достаточно канонических `Article Template` и `Overview Template`;
- не создавать отдельные тематические template-файлы под `Network Security` или `VPN`, потому что по `Principia Rerum` достаточно канонических `Article Template` и `Overview Template`;
- не определять `Server` сразу как машину или только как процесс, потому что это сузит термин раньше, чем будет зафиксирована его role-based рамка;
- не прятать `Packet Switches` внутрь `Network Protocols`, потому что это смешает devices и rules;
- не прятать `VPN` внутрь `Network Protocols` как просто еще один protocol note;
- не заводить заранее плоский каталог всех возможных сетевых устройств без устойчивого корпуса;
- не дублировать `Router` одновременно под `Internet`, `OSI Model` и `Packet Switches`.

## Что стоит раскрыть дальше

- [ ] Решить, когда в `Packet Switches` нужны `Switching Fabric` и `Forwarding Table`
- [ ] Решить, когда рядом с `Client-Server Model` нужны `Load Balancing`, `Service Discovery` и `Backpressure`
- [ ] Решить, когда рядом с `VPN` нужны `Zero Trust Network Access`, `Firewall` и `Network Access Control`
- [ ] Решить, когда нужен отдельный узел про `Packet Forwarding`
- [ ] Проверить границу между `Router` и `Routing`
- [ ] Проверить `related`
