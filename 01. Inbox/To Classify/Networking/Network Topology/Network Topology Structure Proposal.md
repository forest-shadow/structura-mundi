---
aliases:
  - Network Topology Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-topology
parent: "[[Networking]]"
status: draft
related:
  - "[[Networking]]"
  - "[[Network Topology]]"
  - "[[Common Network Topologies]]"
  - "[[Physical and Logical Network Topology]]"
tags: []
---

# Network Topology Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Network Topology` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Network Topology
    ├── Physical and Logical Network Topology
    └── Common Network Topologies
        ├── Point-to-Point Network Topology
        ├── Bus Network Topology
        ├── Star Network Topology
        ├── Ring Network Topology
        ├── Mesh Network Topology
        ├── Tree Network Topology
        └── Hybrid Network Topology
```

## Почему структура именно такая

- `Network Topology` уже оправдан как `sub-overview`, потому что тема естественно распадается как минимум на различие physical/logical topology и на устойчивый набор именованных topology patterns.
- `Physical and Logical Network Topology` лучше держать отдельной статьей, потому что это не просто вводный подраздел, а базовая понятийная развилка для всей ветки.
- `Common Network Topologies` лучше оформить как вложенный `sub-overview`, чтобы не превращать `Network Topology` в длинный плоский список слабо связанных leaf-заметок.
- Отдельные topology patterns вроде `Star Network Topology` и `Mesh Network Topology` заслуживают собственных notes, потому что у каждого есть собственный профиль связности, отказоустойчивости и operational trade-offs.
- Более специальные темы вроде spine-leaf, Clos, campus topology и WAN topology пока создавать не нужно: сначала стоит заполнить базовую ветку.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Network Topology` внутрь `Internet`: тема шире, чем организация современной Internet.
- Не стоит создавать отдельные заметки про каждый исторический или vendor-specific дизайн сети.
- Не стоит дублировать каждый topology pattern отдельными notes для `physical` и `logical`, если различие пока достаточно раскрывать внутри существующих статей.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен `Datacenter Network Topology`
- [ ] Проверить, нужен ли рядом отдельный узел про `Network Redundancy`
- [ ] Проверить `related`
