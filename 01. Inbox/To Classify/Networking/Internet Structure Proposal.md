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
    ├── DNS
    └── Routing
```

## Почему структура именно такая

- `Internet` уже оправдан как `sub-overview`, потому что рассмотрение Internet не сводится к одному определению и требует хотя бы адресации, маршрутизации, naming и протокольной архитектуры.
- `TCP IP Model` логично делать дочерней overview-веткой именно `Internet`, потому что Internet protocol suite описывает архитектурный стек самой Internet.
- `IP Addressing`, `DNS` и `Routing` достаточно самостоятельны для отдельных article-notes, но пока не требуют дополнительных промежуточных overview-узлов.

## Что не стоит делать прямо сейчас

- Не стоит заранее выносить `TCP`, `UDP`, `HTTP`, `BGP` и `NAT` в отдельные article без плотного корпуса рядом.
- Не стоит смешивать Internet branch с purely conceptual `OSI Model`.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `TCP`, `UDP` и `HTTP`
- [ ] Проверить `related`
