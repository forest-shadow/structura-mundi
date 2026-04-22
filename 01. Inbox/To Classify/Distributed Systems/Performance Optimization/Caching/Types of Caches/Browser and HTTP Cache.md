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
  - "[[CDN and Edge Cache]]"
  - "[[Cache Invalidation]]"
tags: []
---

# Browser and HTTP Cache

## Краткое определение

`Browser and HTTP Cache` — это статья о клиентском и protocol-level кэшировании, где freshness и reuse управляются HTTP semantics, headers и поведением user agent.

## Границы темы

- Входит: browser cache, shared HTTP cache, cache-control driven freshness.
- Не входит: CDN как отдельный edge layer и не входит application in-memory cache.

## Связи с другими заметками

Родительская тема:

`[[Types of Caches]]`

Связанные заметки:

- `[[CDN and Edge Cache]]`
- `[[Cache Invalidation]]`
- `[[Expiration Policies]]`

## Примеры, случаи или следствия

- HTTP cache снижает latency и bandwidth consumption без обязательного обращения к origin.
- Неверно выставленные freshness rules легко приводят либо к stale content, либо к потере cache hit rate.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `HTTP Cache-Control`
- [ ] Проверить `related`
