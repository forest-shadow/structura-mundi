---
aliases:
  - Proxy Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-protocols
parent: "[[HTTP]]"
status: draft
related:
  - "[[Proxy]]"
  - "[[HTTP]]"
  - "[[Forward Proxy]]"
  - "[[Reverse Proxy]]"
tags: []
---

# Proxy Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Proxy` внутри `HTTP`.

## Рекомендуемая иерархия

```text
HTTP
└── Proxy
    ├── Forward Proxy
    └── Reverse Proxy
```

## Почему структура именно такая

- `Proxy` здесь лучше оформлять как вложенный `overview`, а не как одну статью, потому что тема естественно распадается минимум на две разные посреднические роли: клиентскую и серверную.
- `Forward Proxy` нужен как отдельный article, чтобы не сводить всю тему прокси только к server-side инфраструктуре и явно показать точку зрения клиента.
- `Reverse Proxy` нужен как отдельный article, потому что вокруг него быстро собираются устойчивые механизмы вроде TLS termination, request routing, origin shielding, caching и load balancing.
- Подчинять `Proxy` напрямую `Application Layer Protocols` пока не стоит: в текущей структуре vault именно `HTTP` уже удерживает рамку request-response взаимодействия и промежуточных HTTP-узлов.
- Отдельный `section` для proxy-ветки пока не нужен: существующего `section: network-protocols` достаточно, потому что ветка остается компактной и живет внутри уже оформленного HTTP-кластера.

## Что не стоит делать прямо сейчас

- Не стоит заранее создавать отдельные notes про `Transparent Proxy`, `Open Proxy`, `Proxy Chaining` или `Proxy Authentication`, пока базовая ветка не заполнена.
- Не стоит смешивать в одной статье `Proxy`, `Load Balancer`, `API Gateway` и `CDN`, даже если между ними есть пересечения по инфраструктурной роли.
- Не стоит заводить vendor-specific notes вроде `Nginx`, `HAProxy` или `Envoy` как часть этой ветки, пока не появится устойчивый корпус по самим понятиям.

## Созданные черновые заметки

- `Proxy.md`
- `Forward Proxy.md`
- `Reverse Proxy.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить, что `Proxy` остается вложенной HTTP-веткой, а не выносится в отдельный infrastructure-кластер рядом с `HTTP`.
2. Решить, когда рядом понадобятся `Load Balancer`, `API Gateway` и `CDN and Edge Cache` как соседние или пересекающиеся темы.
3. Наполнить `Reverse Proxy` так, чтобы его границы с `Forward Proxy` и `CDN` были явно различимы уже на уровне обзора.
