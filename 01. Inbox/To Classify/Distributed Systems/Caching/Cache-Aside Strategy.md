---
aliases:
  - Lazy Loading Cache
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Caching Strategies]]"
status: seed
related:
  - "[[Caching Strategies]]"
  - "[[Cache Invalidation]]"
  - "[[Distributed Cache]]"
  - "[[Write-Through and Write-Back Caching]]"
tags: []
---

# Cache-Aside Strategy

## Краткое определение

`Cache-Aside Strategy` — это статья о паттерне, в котором приложение само управляет чтением из кэша, fallback к source of truth и последующим наполнением кэша.

## Границы темы

- Входит: cache-aside как application-level read path strategy.
- Не входит: write-path strategies вроде write-through и write-back.

## Связи с другими заметками

Родительская тема:

`[[Caching Strategies]]`

Связанные заметки:

- `[[Cache Invalidation]]`
- `[[Write-Through and Write-Back Caching]]`
- `[[Distributed Cache]]`

## Примеры, случаи или следствия

- Cache miss ведет к чтению из primary store и последующему populate кэша.
- Простота cache-aside делает его популярным, но invalidation и stampede остаются отдельными проблемами.

## Что стоит раскрыть дальше

- [ ] Добавить связь с miss penalty и warmup behavior
- [ ] Проверить `related`
