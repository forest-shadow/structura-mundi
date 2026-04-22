---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Performance Optimization]]"
status: seed
related:
  - "[[Distributed Systems]]"
  - "[[Performance Optimization]]"
  - "[[Distributed Systems Problems]]"
  - "[[Types of Caches]]"
  - "[[Caching Strategies]]"
  - "[[Cache Invalidation]]"
  - "[[Cache Policies]]"
tags: []
---

# Caching

## Краткое определение области

`Caching` — это обзорная заметка про использование кэша в распределенных системах как механизма снижения latency, разгрузки источника истины и управления trade-offs между скоростью, свежестью данных и сложностью координации.

## Что входит в эту тему

- `[[Types of Caches]]`
- `[[Caching Strategies]]`
- `[[Cache Invalidation]]`
- `[[Cache Policies]]`
- `[[Cache Stampede]]`

## Как устроена ветка

- `Types of Caches` раскладывает основные виды кэшей по месту и роли в системе.
- `Caching Strategies` собирает operational patterns чтения и записи через кэш, чтобы стратегии не смешивались с остальными concept-notes.
- `Cache Invalidation` теперь собирает отдельные механизмы протухания, purge и version-driven freshness control.
- `Cache Policies` отделяет правила admission, expiration и eviction от стратегий и видов кэша.
- `Cache Stampede` фиксирует типичную failure/performance pathology, возникающую вокруг popular keys и массовых промахов.

## Рекомендуемый маршрут чтения

1. Начать с `[[Caching Strategies]]`, чтобы увидеть базовые модели чтения и записи через кэш.
2. Затем перейти к `[[Cache Invalidation]]`.
3. После этого читать `[[Cache Policies]]`.
4. Затем перейти к `[[Types of Caches]]`.
5. Завершить `[[Cache Stampede]]` как типичным failure mode caching-ветки.

## Соседние overview-ветки

- `[[Performance Optimization]]`
- `[[Load Balancing]]`
- `[[Backpressure and Flow Control]]`
- `[[Distributed Systems Problems]]`
- `[[Telemetry]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Request Coalescing`
- [ ] Решить, когда нужен отдельный article про `Near Cache`
- [ ] Проверить `related`
