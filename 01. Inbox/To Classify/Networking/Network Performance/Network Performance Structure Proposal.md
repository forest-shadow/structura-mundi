---
aliases:
  - Network Performance Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-performance
parent: "[[Networking]]"
status: draft
related:
  - "[[Networking]]"
  - "[[Network Performance]]"
  - "[[Network Bandwidth]]"
  - "[[Network Throughput]]"
tags: []
---

# Network Performance Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Network Performance` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Network Performance
    ├── Network Bandwidth
    ├── Network Throughput
    ├── Network Latency
    ├── Network Jitter
    └── Network Packet Loss
```

## Почему структура именно такая

- `Network Performance` уже оправдан как `sub-overview`, потому что тема естественно распадается на устойчивый набор performance metrics, которые постоянно сопоставляются друг с другом.
- `Network Bandwidth` не стоит оставлять одиночной статьей под `Networking`, потому что без соседних notes про throughput, latency и loss тема остается концептуально неполной.
- `Network Throughput` нужен как самостоятельная статья, потому что путаница между bandwidth и throughput слишком типична, чтобы держать throughput только мелким разделом.
- `Network Latency`, `Network Jitter` и `Network Packet Loss` образуют минимальный дополнительный слой метрик качества, без которого performance-ветка сводится только к одной оси capacity.
- Более специальные темы вроде `Bandwidth-Delay Product`, `Network Congestion`, `QoS` и `Traffic Shaping` пока не нужно выносить отдельно: сначала стоит заполнить базовый кластер.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Network Bandwidth` внутрь `Internet`, потому что это более общая networking-тема, а не аспект только Internet.
- Не стоит дробить ветку на слишком тонкие operational notes вроде отдельных статей про Mbps, Gbps и line rate.
- Не стоит создавать `Bandwidth vs Throughput` как отдельную note, если различие пока естественно раскрывается через две базовые статьи и overview.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Bandwidth-Delay Product` и `Network Congestion`
- [ ] Проверить, нужен ли рядом `Quality of Service`
- [ ] Проверить `related`
