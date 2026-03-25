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
  - "[[Cache-Aside Strategy]]"
  - "[[Distributed Cache]]"
tags: []
---

# Application Cache

## Краткое определение

`Application Cache` — это статья о кэше, который живёт внутри процесса приложения или рядом с ним и используется для ускорения повторных чтений без обязательного сетевого hop.

## Границы темы

- Входит: in-memory cache в сервисе, локальный cache layer, service-level hot data.
- Не входит: shared distributed cache как отдельная инфраструктура.

## Связи с другими заметками

Родительская тема:

`[[Types of Caches]]`

Связанные заметки:

- `[[Cache-Aside Strategy]]`
- `[[Distributed Cache]]`
- `[[Cache Invalidation]]`

## Примеры, случаи или следствия

- Локальный кэш даёт минимальную latency, но усложняет согласованность между инстансами.
- Чем больше replicas у сервиса, тем заметнее становится проблема stale local copies.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Near Cache`
- [ ] Проверить `related`
