# Network Security Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Network Security` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Network Security
    └── VPN
        ├── Remote Access VPN
        ├── Site-to-Site VPN
        ├── VPN Tunneling
        └── VPN Protocol Families
```

## Почему структура именно такая

- `Network Security` уже оправдана как `sub-overview`, потому что VPN неестественно прятать прямо под `Networking` без security-рамки.
- `VPN` лучше оформлять как отдельный `sub-overview`, а не как одиночный article, потому что внутри темы быстро возникают разные типы развертывания, способы туннелирования и семейства протоколов.
- `Remote Access VPN` и `Site-to-Site VPN` логично держать отдельно, потому что это два разных operational pattern.
- `VPN Tunneling` лучше отделять от deployment patterns, чтобы не смешивать тип канала с типом сценария использования.
- `VPN Protocol Families` нужен как промежуточный article, чтобы не плодить сразу notes про `IPsec`, `OpenVPN`, `WireGuard`, `L2TP` и `SSL VPN` без устойчивого корпуса рядом.

## Что не стоит делать прямо сейчас

- Не стоит прятать `VPN` внутрь `Network Protocols` как просто еще один протокол.
- Не стоит сразу создавать плоский каталог из `IPsec`, `WireGuard`, `OpenVPN`, `PPTP` и `L2TP` без заполненной базовой VPN-ветки.
- Не стоит смешивать в одной заметке сценарии развертывания, туннелирование и протокольные семейства.

## Что стоит раскрыть дальше

- [ ] Решить, когда `VPN Protocol Families` превращается в отдельный `sub-overview`
- [ ] Решить, когда рядом нужны `SSL VPN` и `IPsec VPN`
- [ ] Проверить `related`
