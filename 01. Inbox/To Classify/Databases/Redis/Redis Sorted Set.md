---
aliases:
  - ZSET
  - Redis ZSET
note_type: article
area: computer-science
domain: databases
section: redis
parent: "[[Redis]]"
status: seed
related:
  - "[[Distributed Cache]]"
tags: []
---

# Redis Sorted Set

## Краткое определение

`Redis Sorted Set` — это Redis-структура данных, в которой уникальные элементы упорядочиваются по score и позволяют эффективно работать с рейтингами, лидербордами, приоритетами и range-запросами.

## Основная идея или механизм

Эта заметка может раскрывать:

- что такое score-based ordering в Redis;
- чем `Redis Sorted Set` отличается от обычного `Set` и от других Redis data types;
- почему именно этот примитив удобен для leaderboards, top-N и range-by-score сценариев.

## Границы темы

- В тему входят модель данных, роль score, типовые операции и практические сценарии применения.
- Рядом, но не тождественно теме, находятся общие заметки про `Redis`, caching use cases и конкретные command-level детали, если они начинают разрастаться отдельно.

## Связи с другими заметками

Родительская тема:

- `[[Redis]]`

Связанные заметки:

- `[[Distributed Cache]]`

## Примеры, случаи или следствия

- `Redis Sorted Set` подходит для leaderboard-сценариев, где важно быстро получать top-N и соседей по рангу.
- Он удобен для time-ordered или score-ordered выборок, когда plain `Set` уже не хватает.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между ordered-by-score и plain set semantics
- [ ] Добавить типовые сценарии применения
- [ ] Проверить `aliases`
- [ ] Проверить `related`
