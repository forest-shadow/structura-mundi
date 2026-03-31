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
  - "[[Proxy]]"
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
    ├── HTTP Versions
    └── Proxy
        ├── Forward Proxy
        └── Reverse Proxy
```

## Почему структура именно такая

- `HTTP` уже оправдан как `sub-overview`, потому что тема быстро распадается на несколько устойчивых аспектов, которые слишком велики для одного article.
- `HTTP Messages` лучше держать отдельной статьей, потому что без нее остальные элементы HTTP остаются без общей request-response рамки.
- `HTTP Methods`, `HTTP Status Codes` и `HTTP Header Fields` заслуживают собственных notes, потому что это канонические и часто отдельно изучаемые части протокола.
- `HTTP Versions` лучше вынести отдельно, потому что версия протокола — это не просто очередной раздел про синтаксис, а отдельная линия эволюции HTTP.
- `Proxy` оправдан как вложенный `sub-overview`, потому что тема HTTP включает устойчивый класс промежуточных узлов, а различие между `Forward Proxy` и `Reverse Proxy` слишком смысловое, чтобы держать его одной плоской статьей.
- `Forward Proxy` и `Reverse Proxy` полезно разводить по разным notes, потому что они смотрят на проксирование с разных сторон trust boundary и решают разные задачи.
- Более узкие темы вроде cookies, caching, authentication и content negotiation пока не нужно выносить, пока базовая ветка не заполнена.

## Что не стоит делать прямо сейчас

- Не стоит называть каноничную note `HTTP Protocols`, если речь идет об одном protocol family с версиями; сильнее работает просто `HTTP`.
- Не стоит сразу дробить ветку на десятки мелких notes про каждый status code или каждый header field.
- Не стоит смешивать protocol semantics, browser behavior и web architecture в одной и той же overview-note.
- Не стоит сразу смешивать `Proxy`, `Load Balancer`, `API Gateway` и `CDN` в один общий infrastructure-узел без самостоятельного корпуса по каждой теме.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `HTTP Caching`, `Content Negotiation` и `Cookies`
- [ ] Проверить, нужен ли отдельный узел про `HTTP Semantics`
- [ ] Решить, когда рядом с `Proxy` нужны `Load Balancer` и `API Gateway`
- [ ] Проверить `related`
