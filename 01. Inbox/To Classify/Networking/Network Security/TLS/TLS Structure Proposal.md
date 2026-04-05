---
aliases:
  - TLS Structure Proposal
  - Transport Layer Security Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[Network Security]]"
status: draft
related:
  - "[[TLS]]"
  - "[[Network Security]]"
  - "[[TLS Handshake]]"
  - "[[TLS Certificate Validation]]"
  - "[[Mutual TLS]]"
  - "[[TLS Termination]]"
tags: []
---

# TLS Structure Proposal

## Краткое определение

Предлагаемая иерархия заметок для ветки `TLS` внутри `Network Security`.

## Рекомендуемая иерархия

```text
Network Security
└── TLS
    ├── TLS Handshake
    ├── TLS Certificate Validation
    ├── Mutual TLS
    └── TLS Termination
```

## Почему структура именно такая

- `TLS` оправдан как отдельный overview, потому что тема уже естественно распадается на несколько устойчивых article-слоев.
- `TLS Handshake` лучше держать отдельно, потому что это базовый protocol-flow, без которого трудно понимать остальную ветку.
- `TLS Certificate Validation` стоит выделить отдельно, потому что trust establishment и certificate chain checking — это отдельный аналитический слой, не совпадающий с самим handshake как sequence of messages.
- `Mutual TLS` лучше держать sibling-статьей, потому что это не отдельный протокол, а особый deployment and authentication pattern поверх TLS.
- `TLS Termination` стоит логически держать внутри TLS-ветки, но связывать с `Proxy`, `Service Mesh` и `Origin Shielding` через `related`, а не превращать в дочернюю тему proxy-ветки.

## Что не стоит делать прямо сейчас

- Не стоит раскладывать TLS сразу на notes про каждый cipher suite, extension и alert code.
- Не стоит смешивать в одной заметке handshake, certificate validation, mTLS и termination.
- Не стоит создавать специальные template-файлы под TLS: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный узел про `TLS Versions`
- [ ] Проверить, когда `TLS Certificate Validation` потребует соседнюю note про certificate chain
- [ ] Проверить `related`
