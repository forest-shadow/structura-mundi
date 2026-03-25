---
aliases:
  - Internet Structure Proposal
note_type: article
area: computer-science
domain: networking
section: internet
parent: "[[Networking]]"
status: draft
related:
  - "[[Internet]]"
  - "[[TCP IP Model]]"
  - "[[OSI Model]]"
tags: []
---

# Internet Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Internet` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Internet
    ├── TCP IP Model
    │   ├── TCP IP Link Layer
    │   ├── TCP IP Internet Layer
    │   ├── TCP IP Transport Layer
    │   └── TCP IP Application Layer
    ├── IP Addressing
    ├── Routing
    └── DNS
        ├── DNS Resolution
        ├── Recursive Resolver
        ├── Authoritative DNS Server
        ├── DNS Resource Record
        └── DNS Zone
```

## Почему структура именно такая

- `Internet` уже оправдан как `sub-overview`, потому что рассмотрение Internet не сводится к одному определению и требует хотя бы адресации, маршрутизации, naming и протокольной архитектуры.
- `TCP IP Model` логично делать дочерней overview-веткой именно `Internet`, потому что Internet protocol suite описывает архитектурный стек самой Internet.
- `IP Addressing` и `Routing` достаточно самостоятельны для отдельных article-notes и пока не требуют промежуточных overview-узлов.
- `DNS` уже лучше оформлять как отдельный `sub-overview`, потому что внутри него быстро возникает собственный устойчивый кластер: resolution, resolver role, authoritative role и базовые сущности данных.

## Что не стоит делать прямо сейчас

- Не стоит заранее выносить `TCP`, `UDP`, `HTTP`, `BGP` и `NAT` в отдельные article без плотного корпуса рядом.
- Не стоит смешивать Internet branch с purely conceptual `OSI Model`.
- Не стоит преждевременно дробить DNS еще глубже на `Root Name Server`, `DNSSEC` и `Zone Transfer`, пока базовая DNS-ветка не наполнена.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `TCP`, `UDP` и `HTTP`
- [ ] Подтвердить, нужен ли для DNS отдельный `section: dns`
- [ ] Проверить `related`
