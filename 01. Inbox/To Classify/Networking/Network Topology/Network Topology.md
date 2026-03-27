---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-topology
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[OSI Model]]"
  - "[[Physical Layer]]"
  - "[[Common Network Topologies]]"
  - "[[Physical and Logical Network Topology]]"
tags: []
---

# Network Topology

## Краткое определение области

`Network Topology` — это обзорная заметка о том, как в сети организованы узлы и связи между ними и как эта организация влияет на связность, отказоустойчивость, масштабируемость и стоимость сети.

## Что входит в эту тему

- `[[Physical and Logical Network Topology]]`
- `[[Common Network Topologies]]`

## Как устроена ветка

- `Network Topology` служит общей рамкой для разговора о форме и организации сетей, а не о конкретных протоколах.
- `Physical and Logical Network Topology` фиксирует базовое различие между физическим размещением связей и логической схемой обмена.
- `Common Network Topologies` собирает устойчивые канонические паттерны вроде `star`, `ring`, `mesh` и `tree`.
- Более узкие темы вроде конкретных Ethernet-дизайнов, datacenter fabrics или wireless mesh пока не выносятся в отдельные статьи, чтобы ветка не разрасталась преждевременно.

## Рекомендуемый маршрут чтения

1. Начать с `[[Physical and Logical Network Topology]]`, чтобы зафиксировать базовые оси различения.
2. Затем перейти к `[[Common Network Topologies]]`.
3. После этого читать отдельные паттерны внутри `Common Network Topologies` и сопоставлять их с `[[OSI Model]]` и `[[Routing]]`, если нужен более инженерный взгляд.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Соседняя model-ветка: `[[OSI Model]]`
- Соседняя operational-ветка: `[[Internet]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные статьи про `Datacenter Topology` и `Wireless Mesh Network`
- [ ] Проверить, нужен ли отдельный узел про `Network Redundancy`
- [ ] Проверить `related`
