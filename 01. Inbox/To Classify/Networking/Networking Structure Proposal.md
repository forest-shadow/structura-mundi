# Networking Structure Proposal

## Назначение

Этот файл фиксирует рабочую иерархию domain-root ветки `Networking` внутри `Computer Science` по правилам `Principia Rerum`.

Словарная рамка для рабочей ветки:

- `domain: networking`
- `section: network-topology`
- `section: network-performance`
- `section: network-protocols`
- `section: internet`
- `section: dns`
- `section: network-models`
- `section: packet-switches`

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
- `Packet Switches` лучше держать отдельной sibling-веткой рядом с `Network Protocols` и `Internet`, потому что устройства пересылки пакетов и кадров образуют собственный понятийный кластер.
- `Router` и `Link-Layer Switch` логично собирать под `Packet Switches`, а не разносить по разным моделям стека, потому что здесь важнее их общая роль forwarding devices.
- `Network Protocols` лучше не смешивать с `Packet Switches`: протоколы описывают правила взаимодействия, а switches и routers являются устройствами, реализующими пересылку и коммутацию.
- `Internet` остаётся отдельной operational-веткой про современную сетевую среду, где routing и addressing рассматриваются как рабочие механизмы реального интернета.
- `OSI Model` и `TCP IP Model` остаются model-centric ветками, а не контейнерами для всех device notes.

## Что не стоит делать прямо сейчас

- не создавать отдельные тематические template-файлы под Networking или Packet Switches, потому что по `Principia Rerum` достаточно канонических `Article Template` и `Overview Template`;
- не прятать `Packet Switches` внутрь `Network Protocols`, потому что это смешает devices и rules;
- не заводить заранее плоский каталог всех возможных сетевых устройств без устойчивого корпуса;
- не дублировать `Router` одновременно под `Internet`, `OSI Model` и `Packet Switches`.

## Что стоит раскрыть дальше

- [ ] Решить, когда в `Packet Switches` нужны `Switching Fabric` и `Forwarding Table`
- [ ] Решить, когда нужен отдельный узел про `Packet Forwarding`
- [ ] Проверить границу между `Router` и `Routing`
- [ ] Проверить `related`
