# Networking Structure Proposal

## Назначение

Этот файл фиксирует рабочую иерархию domain-root ветки `Networking` внутри `Computer Science` по правилам `Principia Rerum`.

Словарная рамка для рабочей ветки:

- `domain: networking`
- `section: network-topology`
- `section: network-performance`
- `section: network-protocols`
- `section: traffic-intermediation`
- `section: network-security`
- `section: internet`
- `section: dns`
- `section: network-models`
- `section: packet-switches`

## Рекомендуемая иерархия

```text
Computer Science
└── Networking
    ├── Network Interaction Models
    │   ├── Client-Server Model
    │   │   ├── Client
    │   │   └── Server
    │   │       ├── Server Application
    │   │       ├── Server Process
    │   │       │   ├── Network Listener
    │   │       │   ├── Request Handling
    │   │       │   ├── Server Concurrency Model
    │   │       │   ├── Server Lifecycle Management
    │   │       │   ├── Timeouts and Cancellation
    │   │       │   ├── Server Observability
    │   │       │   └── Server Resource Management
    │   │       ├── Server Host
    │   │       └── Service Endpoint
    │   ├── Peer-to-Peer Model
    │   ├── Request-Reply Model
    │   └── Broadcast and Multicast Model
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
    ├── Proxy
    │   ├── Proxy Roles
    │   │   ├── Forward Proxy
    │   │   └── Reverse Proxy
    │   ├── Proxy Interception Models
    │   │   ├── Explicit Proxy
    │   │   ├── Transparent Proxy
    │   │   └── Intercepting Proxy
    │   ├── Proxy Processing Models
    │   │   ├── Circuit-Level Proxy
    │   │   ├── Application-Level Proxy
    │   │   ├── Layer 4 Proxy
    │   │   └── Layer 7 Proxy
    │   ├── Proxy Protocols and Mechanisms
    │   │   ├── HTTP Proxy
    │   │   ├── SOCKS Proxy
    │   │   ├── CONNECT Tunneling
    │   │   ├── Proxy Authentication
    │   │   └── Proxy Chaining
    │   └── Proxy Functions
    ├── Service Mesh
    │   ├── Service Mesh Control Plane
    │   ├── Service Mesh Data Plane
    │   └── Istio
    ├── Origin Shielding
    ├── Network Security
    │   ├── Slowloris Attack
    │   ├── TLS
    │   │   ├── TLS Handshake
    │   │   ├── TLS Certificate Validation
    │   │   ├── Mutual TLS
    │   │   └── TLS Termination
    │   └── VPN
    │       ├── Remote Access VPN
    │       ├── Site-to-Site VPN
    │       ├── VPN Tunneling
    │       └── VPN Protocol Families
    ├── Packet Switches
    │   ├── Router
    │   └── Link-Layer Switch
    ├── Internet
    │   ├── Network Edge
    │   │   ├── End System
    │   │   └── Access Network
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
- `Network Interaction Models` уместно держать как отдельный `sub-overview`, потому что здесь нужен самостоятельный model-centric язык для базовых форм сетевого обмена между узлами.
- `Client-Server Model` остается одной из этих моделей, но больше не висит напрямую под domain-root, потому что рядом появились другие interaction-level siblings.
- `Server` лучше оформлять как `overview`, а не как одну перегруженную `article`, потому что термин одновременно живет на уровне роли, программного компонента, процесса, хоста и сетевой точки входа.
- `Server Process` тоже оправдан как вложенный `overview`, потому что вокруг него уже возникает устойчивый operational cluster: listener, request handling, concurrency, lifecycle, timeouts, observability и resource management.
- `Packet Switches` лучше держать отдельной sibling-веткой рядом с `Network Protocols` и `Internet`, потому что устройства пересылки пакетов и кадров образуют собственный понятийный кластер.
- `Network Security` оправдана как отдельная sibling-ветка рядом с `Network Protocols` и `Internet`, потому что защищенный сетевой доступ, trust boundaries и protocol-level protection образуют собственный понятийный кластер.
- `Slowloris Attack` пока уместно держать как обычную `article` внутри `Network Security`, а не как начало отдельного attack-cluster, потому что без соседних заметок про другие DoS-атаки новый `overview` был бы преждевременным.
- `TLS` лучше оформлять как `sub-overview` внутри `Network Security`, потому что тема уже естественно распадается на handshake, certificate validation, mTLS и termination.
- `TLS Termination` логически лучше жить внутри `TLS`, потому что без общей protocol-and-trust рамки она быстро превращается в чисто инфраструктурный прием и теряет смысловые границы.
- `Proxy`, `Service Mesh` и `Origin Shielding` по-прежнему образуют intermediary-layer cluster; `TLS Termination` остается с ним тесно связанной cross-cutting темой через `related`.
- `VPN` лучше оформлять как `sub-overview`, а не как одиночный article, потому что внутри темы быстро возникают разные deployment patterns, tunnel mechanics и protocol families.
- `Router` и `Link-Layer Switch` логично собирать под `Packet Switches`, а не разносить по разным моделям стека, потому что здесь важнее их общая роль forwarding devices.
- `Network Protocols` лучше не смешивать с `Packet Switches`: протоколы описывают правила взаимодействия, а switches и routers являются устройствами, реализующими пересылку и коммутацию.
- `Service Mesh` лучше держать sibling-веткой рядом с `Proxy`, а не внутри него, потому что service mesh включает не только proxying, но и control-plane coordination для service-to-service traffic.
- `VPN` не стоит прятать напрямую под `Internet` или `Network Protocols`, потому что тема VPN описывает не только протокол, но и security pattern защищенного логического канала поверх недоверенной сети.
- `Internet` остаётся отдельной operational-веткой про современную сетевую среду, где routing и addressing рассматриваются как рабочие механизмы реального интернета.
- `Network Edge` логично держать внутри `Internet`, а не в `Network Interaction Models`, потому что это infrastructural-ветка, собирающая hosts и access connectivity, а не role-based формы обмена.
- `End System` лучше оставить обычной `article`, потому что desktops, smartphones и servers здесь являются примерами одного устойчивого класса hosts, а не самостоятельными дочерними узлами.
- `Access Network` оправдана как sibling-статья рядом с `End System`, потому что описывает подключение к Internet, а не саму конечную систему.
- `OSI Model` и `TCP IP Model` остаются model-centric ветками, а не контейнерами для всех device notes.

## Что не стоит делать прямо сейчас

- не создавать отдельные тематические template-файлы под Networking, TLS или Network Security, потому что по `Principia Rerum` достаточно канонических `Article Template` и `Overview Template`;
- не определять `TLS` сразу как каталог всех криптографических примитивов: ветка должна оставаться сетевой и operationally useful;
- не создавать отдельные notes под каждый cipher suite, alert code или extension до появления устойчивого корпуса;
- не смешивать в одной заметке protocol-level устройство TLS, trust model и инфраструктурные deployment patterns.

## Что стоит раскрыть дальше

- [ ] Решить, когда внутри `TLS` нужны `TLS Versions` и `TLS Resumption`
- [ ] Проверить границу между `TLS`, `TLS Termination`, `Proxy`, `Service Mesh` и `Origin Shielding`
- [ ] Решить, когда рядом с `VPN` нужны `Zero Trust Network Access`, `Firewall` и `Network Access Control`
- [ ] Решить, когда нужен отдельный узел про `Packet Forwarding`
- [ ] Проверить границу между `Router` и `Routing`
- [ ] Проверить `related`
