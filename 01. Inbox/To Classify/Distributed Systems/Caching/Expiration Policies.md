---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Cache Policies]]"
status: seed
related:
  - "[[Cache Policies]]"
  - "[[TTL-Based Invalidation]]"
  - "[[Stale-While-Revalidate]]"
tags: []
---

# Expiration Policies

## Краткое определение

`Expiration Policies` — это статья о правилах, по которым объект считается слишком старым для нормальной выдачи из кэша.

## Границы темы

- Входит: hard TTL, soft TTL, sliding expiration, freshness windows.
- Не входит: eviction by capacity pressure и не входит event-driven invalidation.

## Связи с другими заметками

Родительская тема:

`[[Cache Policies]]`

Связанные заметки:

- `[[TTL-Based Invalidation]]`
- `[[Stale-While-Revalidate]]`
- `[[Cache Invalidation]]`

## Примеры, случаи или следствия

- Expiration policy определяет баланс между freshness и hit rate.
- Soft TTL часто используется там, где допустимо controlled staleness.

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужен отдельный article про `Soft TTL`
- [ ] Проверить `related`
