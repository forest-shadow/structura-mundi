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
  - "[[Event-Driven Invalidation]]"
  - "[[CDN and Edge Cache]]"
tags: []
---

# Tag-Based Invalidation

## Краткое определение

`Tag-Based Invalidation` — это статья о подходе, в котором объекты кэша связываются с тегами или группами, чтобы потом можно было инвалидировать целые наборы данных одним действием.

## Границы темы

- Входит: surrogate keys, group purge, category-level invalidation.
- Не входит: single-key invalidation и не входит versioned key design как основной механизм.

## Связи с другими заметками

Родительская тема:

`[[Cache Invalidation]]`

Связанные заметки:

- `[[Event-Driven Invalidation]]`
- `[[CDN and Edge Cache]]`
- `[[Version-Based Invalidation]]`

## Примеры, случаи или следствия

- Tag-based invalidation особенно полезен там, где один change event затрагивает много derived objects.
- Цена — необходимость поддерживать правильные зависимости между объектами и tags.

## Что стоит раскрыть дальше

- [ ] Проверить, когда note нужно связать с content delivery workflows
- [ ] Проверить `related`
