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

# Database Cache

## Краткое определение

`Database Cache` — это статья о кэшировании вокруг базы данных: результатов запросов, объектов доступа или frequently requested records.

## Границы темы

- Входит: query cache, result cache, cache layer перед базой.
- Не входит: внутренние page caches СУБД как отдельная тема внутренней архитектуры конкретной database engine.

## Связи с другими заметками

Родительская тема:

`[[Types of Caches]]`

Связанные заметки:

- `[[Cache-Aside Strategy]]`
- `[[Write-Through and Write-Back Caching]]`
- `[[Cache Stampede]]`

## Примеры, случаи или следствия

- Database cache уменьшает load на primary store, но создаёт дополнительные вопросы freshness.
- Популярные запросы особенно чувствительны к stampede и некорректному TTL.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Query Result Cache`
- [ ] Проверить `related`
