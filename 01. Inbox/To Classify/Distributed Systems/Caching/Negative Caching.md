---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Caching Strategies]]"
status: seed
related:
  - "[[Caching Strategies]]"
  - "[[Cache-Aside Strategy]]"
  - "[[TTL-Based Invalidation]]"
tags: []
---

# Negative Caching

## Краткое определение

`Negative Caching` — это статья о кэшировании отрицательных результатов: отсутствующих записей, ошибок доступа или иных повторяющихся negative lookups.

## Границы темы

- Входит: caching misses and absent values как отдельный operational pattern.
- Не входит: общий cache-aside без фиксации negative responses.

## Связи с другими заметками

Родительская тема:

`[[Caching Strategies]]`

Связанные заметки:

- `[[Cache-Aside Strategy]]`
- `[[TTL-Based Invalidation]]`
- `[[Cache Stampede]]`

## Примеры, случаи или следствия

- Negative caching уменьшает повторную нагрузку на источник для отсутствующих ключей.
- Слишком длинный TTL на negative result может закрепить ложное отсутствие данных.

## Что стоит раскрыть дальше

- [ ] Проверить, когда note нужно связать с abuse protection
- [ ] Проверить `related`
