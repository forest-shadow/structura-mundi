---
aliases: []
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Partitioning Strategy Selection]]"
  - "[[Partition Pruning]]"
  - "[[Sharding]]"
tags: []
---

# Partitioning Trade-offs

## Краткое определение

`Partitioning Trade-offs` — это заметка о том, какие выгоды и издержки возникают при внедрении partitioning в реальной базе данных.

## Основная идея или механизм

Partitioning редко бывает бесплатным улучшением. Оно может дать better pruning, более удобный lifecycle management, быстрый archival/drop старых данных и лучшую масштабируемость, но одновременно добавляет сложность маршрутизации, риск data skew, fan-out queries, operational overhead и ограничения на уникальность, индексы и cross-partition operations.

## Границы темы

- Входит: performance benefits, maintenance benefits, skew, hot partitions, fan-out reads, rebalance cost, operational complexity.
- Не входит: выбор конкретной стратегии по workload; это относится к `[[Partitioning Strategy Selection]]`.

## Связи с другими заметками

Родительская тема:

`[[Database Partitioning]]`

Связанные заметки:

- `[[Partitioning Strategy Selection]]`
- `[[Partition Pruning]]`
- `[[Sharding]]`

## Примеры, случаи или следствия

Time-based range partitioning может радикально упростить retention и удаление старых данных, но приводит к горячей последней partition. Hash partitioning помогает балансировать запись, но усложняет range analytics и может заставлять систему делать fan-out reads.

## Что стоит раскрыть дальше

- [ ] Добавить связь с global indexes и uniqueness constraints
- [ ] Уточнить trade-offs для OLTP и analytical workloads
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
