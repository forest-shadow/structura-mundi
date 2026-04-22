---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Cache Invalidation]]"
status: seed
related:
  - "[[Cache Invalidation]]"
  - "[[Cache-Aside Strategy]]"
  - "[[Version-Based Invalidation]]"
tags: []
---

# Event-Driven Invalidation

## Краткое определение

`Event-Driven Invalidation` — это статья о подходе, в котором кэш инвалидируется по факту изменения данных или состояния, а не по одному только времени.

## Границы темы

- Входит: purge on update, invalidation events, change notifications.
- Не входит: purely time-based expiration.

## Связи с другими заметками

Родительская тема:

`[[Cache Invalidation]]`

Связанные заметки:

- `[[Cache-Aside Strategy]]`
- `[[Version-Based Invalidation]]`
- `[[Tag-Based Invalidation]]`

## Примеры, случаи или следствия

- Event-driven invalidation уменьшает stale window, но требует надёжной доставки change signals.
- Чем больше downstream caches, тем важнее fan-out и idempotency invalidation events.

## Что стоит раскрыть дальше

- [ ] Решить, когда note нужно связать с event-driven architecture
- [ ] Проверить `related`
