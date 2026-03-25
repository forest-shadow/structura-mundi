---
aliases:
  - Networking Structure Proposal
note_type: article
area: computer-science
domain: networking
section:
parent: "[[Computer Science]]"
status: draft
related:
  - "[[Networking]]"
  - "[[Internet]]"
  - "[[OSI Model]]"
tags: []
---

# Networking Structure Proposal

## Краткое определение

Предлагаемое устройство domain-root ветки `Networking` внутри `Computer Science`.

## Рекомендуемая иерархия

```text
Computer Science
└── Networking
    ├── Internet
    │   ├── TCP IP Model
    │   │   ├── TCP IP Link Layer
    │   │   ├── TCP IP Internet Layer
    │   │   ├── TCP IP Transport Layer
    │   │   └── TCP IP Application Layer
    │   ├── IP Addressing
    │   ├── DNS
    │   └── Routing
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

- `Networking` оправдан как domain-root overview, потому что внутри него уже есть как минимум две самостоятельные обзорные ветки: operational Internet branch и model-centric OSI branch.
- `Internet` стоит делать отдельным `sub-overview`, потому что это не один isolated concept, а устойчивый кластер вокруг TCP/IP, адресации, маршрутизации и naming.
- `OSI Model` лучше держать sibling-веткой, а не child-узлом `Internet`, потому что это концептуальная модель сетевых функций, а не часть самой Internet topology.

## Что не стоит делать прямо сейчас

- Не стоит плодить отдельный `overview` только ради симметрии между всеми возможными networking subfields.
- Не стоит заранее выносить каждый отдельный протокол в самостоятельную note без плотного корпуса.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный `Network Protocols`
- [ ] Проверить `related`
