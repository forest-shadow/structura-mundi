---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Types of Caches]]"
status: seed
related:
  - "[[Types of Caches]]"
  - "[[Distributed Systems Problems]]"
  - "[[Cache Stampede]]"
  - "[[Version-Based Invalidation]]"
tags: []
---

# Distributed Cache

## Краткое определение

`Distributed Cache` — это статья о кэше, который используется как shared component в распределенной системе и сам становится частью ее topology, consistency trade-offs и failure modes.

## Границы темы

- Входит: distributed cache как shared infrastructure layer.
- Не входит: purely local in-process cache без распределенной координации.

## Связи с другими заметками

Родительская тема:

`[[Types of Caches]]`

Связанные заметки:

- `[[Distributed Systems Problems]]`
- `[[Cache Invalidation]]`
- `[[Cache Stampede]]`

## Примеры, случаи или следствия

- Shared cache снижает нагрузку на primary datastore, но добавляет сетевой hop и новые failure modes.
- В distributed cache stale data и partition behavior становятся не только приложенческой, но и системной проблемой.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про replication и sharding в cache layer
- [ ] Проверить `related`
