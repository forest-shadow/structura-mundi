---
aliases:
  - Time & Ordering Proposal
  - Time and Ordering Proposal
  - Time and Ordering Branch Structure Proposal
note_type: article
area: computer-science
domain: distributed-systems
section: distributed-systems-problems
parent: "[[Distributed Systems Problems]]"
status: draft
related:
  - "[[Time and Ordering]]"
  - "[[Clock Synchronization]]"
  - "[[UTC]]"
  - "[[Distributed Systems Problems]]"
  - "[[Coordination and Consensus]]"
  - "[[Consistency Under Replication]]"
tags: []
---

# Time and Ordering Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Time and Ordering` внутри `Distributed Systems Problems` по правилам `Principia Rerum`.

Для этой ветки не требуется новый `section`:

- `area: computer-science`
- `domain: distributed-systems`
- `section: distributed-systems-problems` (переиспользуем существующее рабочее значение)

## Рекомендуемая иерархия

```text
Distributed Systems Problems
└── Time and Ordering
    ├── UTC
    └── Clock Synchronization
```

## Почему структура именно такая

- `Time and Ordering` оправдан как отдельный `overview`, потому что это не одна частная техника, а устойчивый проблемный кластер про physical time, causal order и ограничения локальных наблюдений в distributed systems.
- `UTC` лучше держать как обычную `article`, а не как отдельный `overview`: сама по себе это reference-scale времени, а не крупная подветка с собственным дочерним корпусом.
- `Clock Synchronization` стоит держать рядом отдельной статьёй, потому что она отвечает на другой вопрос: как реальные узлы приближают свои локальные часы к общей внешней шкале вроде `UTC`.
- Отдельные узлы про logical clocks, vector clocks, clock skew и NTP пока преждевременны: на текущем этапе достаточно зафиксировать минимальный каркас ветки и не разрастать её заранее.

## Что не стоит создавать прямо сейчас

- новый `section` под timekeeping или clocks, потому что текущая ветка естественно ложится в уже существующий кластер `distributed-systems-problems`;
- отдельный `sub-overview` вроде `Physical Time`, если внутри ветки пока только два устойчивых дочерних узла;
- отдельные заметки `Time Zone`, `Daylight Saving Time`, `Leap Second`, `Unix Timestamp` и `NTP`, пока они не стали самостоятельными каноническими точками чтения именно в distributed-systems оптике;
- дублировать проблему времени внутри `Coordination and Consensus`, если для неё уже есть собственная обзорная рамка `Time and Ordering`.

## Созданные seed-заготовки

- `[[Time and Ordering]]`
- `[[UTC]]`
- `[[Clock Synchronization]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны отдельные заметки про logical clocks и vector clocks
- [ ] Решить, когда `Clock Synchronization` требует отдельную заметку про `NTP`
- [ ] Уточнить границу между physical time и causal ordering внутри ветки
- [ ] Проверить `related`
