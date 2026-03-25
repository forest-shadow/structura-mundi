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
  - "[[Browser and HTTP Cache]]"
  - "[[Cache Invalidation]]"
tags: []
---

# CDN and Edge Cache

## Краткое определение

`CDN and Edge Cache` — это статья о кэше на сетевой границе, который приближает контент к пользователю и снимает часть нагрузки с origin infrastructure.

## Границы темы

- Входит: edge cache, reverse proxy cache, geo-distributed content caching.
- Не входит: client-side browser cache и не входит shared application cache внутри backend.

## Связи с другими заметками

Родительская тема:

`[[Types of Caches]]`

Связанные заметки:

- `[[Browser and HTTP Cache]]`
- `[[Tag-Based Invalidation]]`
- `[[Expiration Policies]]`

## Примеры, случаи или следствия

- CDN снижает latency для глобальной аудитории и уменьшает нагрузку на origin.
- Чем шире edge footprint, тем важнее управляемая invalidation и purge model.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Reverse Proxy Cache`
- [ ] Проверить `related`
