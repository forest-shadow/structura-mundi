---
aliases:
  - Time-Based Cache Invalidation
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Cache Invalidation]]"
status: seed
related:
  - "[[Cache Invalidation]]"
  - "[[Expiration Policies]]"
  - "[[Negative Caching]]"
tags: []
---

# TTL-Based Invalidation

## Краткое определение

`TTL-Based Invalidation` — это статья о подходе, в котором кэшированный объект считается невалидным после истечения заранее заданного времени жизни.

## Границы темы

- Входит: absolute expiration, time-based freshness windows, TTL as invalidation mechanism.
- Не входит: event-driven или version-based invalidation.

## Связи с другими заметками

Родительская тема:

`[[Cache Invalidation]]`

Связанные заметки:

- `[[Expiration Policies]]`
- `[[Negative Caching]]`
- `[[Cache Stampede]]`

## Примеры, случаи или следствия

- TTL прост в эксплуатации, но плохо реагирует на внезапные изменения данных.
- Одинаковый TTL для популярных ключей может вызывать synchronized expiration.

## Что стоит раскрыть дальше

- [ ] Решить, когда выделять `Soft TTL` и `Hard TTL`
- [ ] Проверить `related`
