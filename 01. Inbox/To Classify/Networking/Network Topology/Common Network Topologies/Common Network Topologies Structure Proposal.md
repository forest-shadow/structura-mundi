---
aliases:
  - Common Network Topologies Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-topology
parent: "[[Network Topology]]"
status: draft
related:
  - "[[Common Network Topologies]]"
  - "[[Network Topology]]"
  - "[[Star Network Topology]]"
  - "[[Mesh Network Topology]]"
tags: []
---

# Common Network Topologies Structure Proposal

## Краткое определение

Предлагаемое устройство вложенной ветки `Common Network Topologies` внутри `Network Topology`.

## Рекомендуемая иерархия

```text
Network Topology
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

- Эта подветка группирует именно именованные topology patterns, а не все возможные разговоры о topology вообще.
- `Point-to-Point`, `Bus`, `Star`, `Ring`, `Mesh` и `Tree` образуют минимальный устойчивый учебный набор базовых patterns.
- `Hybrid Network Topology` полезен как завершающий узел, потому что реальные сети часто комбинируют несколько patterns сразу.
- Дополнительные специальные формы вроде `Spine-Leaf` лучше добавлять позже, когда рядом появится более плотный корпус заметок о современных сетевых архитектурах.

## Что пока не нужно создавать

- `Fully Connected Mesh` и `Partial Mesh` как отдельные заметки, если пока достаточно разделов внутри `Mesh Network Topology`
- `Campus Network Topology` и `Datacenter Network Topology`, если ветка еще не вышла за рамки базовых topology patterns
- Отдельные исторические варианты, если они не образуют собственный устойчивый кластер

## Что стоит раскрыть дальше

- [ ] Решить, когда `Mesh Network Topology` нужно дробить на `Full Mesh` и `Partial Mesh`
- [ ] Проверить `related`
