# Network Security Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Network Security` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Network Security
    ├── Slowloris Attack
    ├── TLS
    │   ├── TLS Handshake
    │   ├── TLS Certificate Validation
    │   ├── Mutual TLS
    │   └── TLS Termination
    └── VPN
        ├── Remote Access VPN
        ├── Site-to-Site VPN
        ├── VPN Tunneling
        └── VPN Protocol Families
```

## Почему структура именно такая

- `Network Security` уже оправдана как `sub-overview`, потому что TLS и VPN неестественно прятать прямо под `Networking` без security-рамки.
- `Slowloris Attack` пока лучше держать как одиночную `article` прямо под `Network Security`, потому что это конкретный класс сетево-прикладной атаки, но вокруг него еще нет достаточного корпуса для отдельного `overview` про DoS-атаки.
- `TLS` лучше оформлять как отдельный `sub-overview`, а не как одиночный article, потому что внутри темы быстро возникают разные protocol-level и trust-level аспекты.
- `TLS Handshake`, `TLS Certificate Validation` и `Mutual TLS` логично держать как sibling-статьи внутри TLS-ветки, потому что это разные аналитические слои одной и той же protocol family.
- `TLS Termination` стоит логически подчинить `TLS`, но сохранять тесную связь с intermediary-layer темами вроде `Proxy` и `Service Mesh` через `related`.
- `VPN` лучше оформлять как отдельный `sub-overview`, а не как одиночный article, потому что внутри темы быстро возникают разные типы развертывания, способы туннелирования и семейства протоколов.
- `Remote Access VPN` и `Site-to-Site VPN` логично держать отдельно, потому что это два разных operational pattern.
- `VPN Tunneling` лучше отделять от deployment patterns, чтобы не смешивать тип канала с типом сценария использования.
- `VPN Protocol Families` нужен как промежуточный article, чтобы не плодить сразу notes про `IPsec`, `OpenVPN`, `WireGuard`, `L2TP` и `SSL VPN` без устойчивого корпуса рядом.

## Что не стоит делать прямо сейчас

- Не стоит прятать `VPN` внутрь `Network Protocols` как просто еще один протокол.
- Не стоит заводить отдельный `overview` вроде `Denial-of-Service Attacks`, пока в ветке нет плотного набора sibling-атак.
- Не стоит раскладывать `TLS` сразу на десятки notes про extensions, cipher suites и alert codes без базовой заполненной ветки.
- Не стоит смешивать в одной заметке handshake, trust model, mTLS и termination.

## Что стоит раскрыть дальше

- [ ] Решить, когда `TLS` потребует `TLS Versions` и `TLS Resumption`
- [ ] Решить, когда `VPN Protocol Families` превращается в отдельный `sub-overview`
- [ ] Решить, когда рядом со `Slowloris Attack` нужны `SYN Flood`, `HTTP Flood` и `Amplification Attack`
- [ ] Проверить границу между `TLS Termination` и intermediary-layer infrastructure
- [ ] Проверить `related`
