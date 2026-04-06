---
aliases:
  - Partitioning Key
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Horizontal Partitioning]]"
  - "[[Partition Pruning]]"
  - "[[Partitioning Strategy Selection]]"
tags: []
---

# Partition Key

## Краткое определение

`Partition Key` — это признак, по которому система определяет, в какую partition попадет запись и через какие partitions будут маршрутизироваться запросы.

## Основная идея или механизм

Выбор partition key определяет почти все практические свойства partitioning: равномерность распределения данных, локальность запросов, вероятность hot partitions, сложность rebalancing и возможность эффективного pruning. Хороший ключ должен одновременно отражать реальный access pattern и не создавать устойчивого перекоса нагрузки.

## Границы темы

- Входит: cardinality, skew, monotonic growth, locality, routing, co-location related data.
- Не входит: конкретная физическая схема разбиения `range/hash/list`; это уже отдельные strategies.

## Связи с другими заметками

Родительская тема:

`[[Database Partitioning]]`

Связанные заметки:

- `[[Horizontal Partitioning]]`
- `[[Partition Pruning]]`
- `[[Partitioning Strategy Selection]]`

## Примеры, случаи или следствия

Ключ по времени удобен для retention и time-based pruning, но может создавать write hotspot на последней partition. Ключ по hash user id лучше балансирует запись и point lookups, но ухудшает range scans и естественную локальность временных данных.

## Что стоит раскрыть дальше

- [ ] Добавить критерии выбора ключа для multi-tenant workloads
- [ ] Уточнить связь между skew и hot partitions
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
