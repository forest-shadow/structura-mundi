---
aliases:
  - Proxy Structure Proposal
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Networking]]"
status: draft
related:
  - "[[Proxy]]"
  - "[[Networking]]"
  - "[[Service Mesh]]"
  - "[[TLS Termination]]"
  - "[[Origin Shielding]]"
tags: []
---

# Proxy Structure Proposal

## Назначение

Этот файл фиксирует общую иерархию заметок для темы `Proxy` по правилам `Principia Rerum`.

Ветка предлагает новый локальный кластер:

- `area: computer-science`
- `domain: networking`
- `section: traffic-intermediation` (предлагаемое новое значение)

`Proxy` здесь понимается как общий класс сетевых посредников, а не как частный случай `HTTP`. Поэтому ветка строится от наиболее общего понятия к нескольким независимым осям классификации, а связи с `HTTP`, `SOCKS`, `TLS Termination` и `Origin Shielding` выражаются через `related`.

## Рекомендуемая иерархия

```text
Networking
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
├── TLS Termination
└── Origin Shielding
```

## Почему структура именно такая

- `Proxy` оправдан как отдельный `sub-overview` под `Networking`, потому что это не просто HTTP-аспект, а более общий класс intermediary nodes.
- Ветка делится не по одной линейной оси, а по нескольким устойчивым классификациям: роль, способ перехвата, модель обработки, протокол/механизм.
- `Proxy Functions` пока лучше держать одной статьей, а не превращать в отдельное дерево из мелких function-notes.
- `TLS Termination` и `Origin Shielding` не стоит прятать внутрь proxy-ветки как дочерние узлы, потому что они шире reverse-proxy-контекста и должны связываться с несколькими соседними темами.
- `HTTP Proxy` следует держать рядом с proxy-механизмами, а не под `HTTP`, потому что это частный способ реализации proxy, а не корневая рамка всей темы.
- `Service Mesh` при появлении собственного корпуса лучше оформлять как соседнюю overview-ветку внутри того же `section: traffic-intermediation`, а не как дочернюю ветку `Proxy`.

## Что не стоит делать прямо сейчас

- Не стоит смешивать `Proxy`, `Load Balancer`, `API Gateway`, `CDN` и `Service Mesh` в один общий overview без отдельного корпуса.
- Не стоит заранее создавать vendor-specific notes вроде `Nginx`, `HAProxy`, `Envoy`, `Squid`.
- Не стоит дробить `Proxy Functions` на отдельные notes про каждую функцию до появления плотного корпуса.

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: traffic-intermediation` как рабочий кластер внутри `domain: networking`.
2. Решить, когда рядом нужны `Load Balancer` и `API Gateway`.
3. Уточнить границы между `Proxy`, `Service Mesh`, `Reverse Proxy`, `Layer 7 Proxy`, `HTTP Proxy` и `CDN and Edge Cache`.
