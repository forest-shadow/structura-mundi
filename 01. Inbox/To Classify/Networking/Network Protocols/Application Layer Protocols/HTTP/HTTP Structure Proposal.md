---
aliases:
  - HTTP Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-protocols
parent: "[[Application Layer Protocols]]"
status: draft
related:
  - "[[HTTP]]"
  - "[[Application Layer Protocols]]"
  - "[[HTTP Messages]]"
  - "[[HTTP Methods]]"
  - "[[HTTP Proxy]]"
tags: []
---

# HTTP Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `HTTP` внутри `Application Layer Protocols`.

## Рекомендуемая иерархия

```text
Application Layer Protocols
└── HTTP
    ├── HTTP Messages
    ├── HTTP Methods
    ├── HTTP Status Codes
    ├── HTTP Header Fields
    └── HTTP Versions
```

## Почему структура именно такая

- `HTTP` уже оправдан как `sub-overview`, потому что тема быстро распадается на несколько устойчивых аспектов, которые слишком велики для одного article.
- `HTTP Messages` лучше держать отдельной статьей, потому что без нее остальные элементы HTTP остаются без общей request-response рамки.
- `HTTP Methods`, `HTTP Status Codes` и `HTTP Header Fields` заслуживают собственных notes, потому что это канонические и часто отдельно изучаемые части протокола.
- `HTTP Versions` лучше вынести отдельно, потому что версия протокола — это не просто очередной раздел про синтаксис, а отдельная линия эволюции HTTP.
- Более узкие темы вроде cookies, caching, authentication и content negotiation пока не нужно выносить, пока базовая ветка не заполнена.

## Что не стоит делать прямо сейчас

- Не стоит называть каноничную note `HTTP Protocols`, если речь идет об одном protocol family с версиями; сильнее работает просто `HTTP`.
- Не стоит сразу дробить ветку на десятки мелких notes про каждый status code или каждый header field.
- Не стоит смешивать protocol semantics, browser behavior и web architecture в одной и той же overview-note.
- Не стоит встраивать общую proxy-онтологию прямо внутрь `HTTP`; сильнее работает отдельная proxy-ветка с перекрестной ссылкой на `HTTP Proxy`.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `HTTP Caching`, `Content Negotiation` и `Cookies`
- [ ] Проверить, нужен ли отдельный узел про `HTTP Semantics`
- [ ] Проверить, нужен ли отдельный article про `HTTP Intermediaries`
- [ ] Проверить `related`
