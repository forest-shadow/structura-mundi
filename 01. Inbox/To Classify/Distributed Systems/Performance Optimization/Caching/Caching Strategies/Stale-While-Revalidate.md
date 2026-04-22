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
  - "[[Read-Through and Refresh-Ahead Caching]]"
  - "[[Cache Stampede]]"
tags: []
---

# Stale-While-Revalidate

## Краткое определение

`Stale-While-Revalidate` — это статья о стратегии, в которой система временно отдаёт устаревшее значение, пока в фоне запрашивает свежую версию.

## Границы темы

- Входит: serving stale data как controlled freshness trade-off ради latency and availability.
- Не входит: общий TTL mechanism без фонового revalidation pattern.

## Связи с другими заметками

Родительская тема:

`[[Caching Strategies]]`

Связанные заметки:

- `[[Read-Through and Refresh-Ahead Caching]]`
- `[[Cache Stampede]]`
- `[[Expiration Policies]]`

## Примеры, случаи или следствия

- Стратегия помогает избегать synchronized misses и улучшает tail latency.
- Цена — осознанное окно controlled staleness.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Request Coalescing`
- [ ] Проверить `related`
