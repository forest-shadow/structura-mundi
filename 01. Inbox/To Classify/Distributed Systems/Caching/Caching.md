---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Distributed Systems]]"
status: seed
related:
  - "[[Distributed Systems]]"
  - "[[Distributed Systems Problems]]"
  - "[[Caching Strategies]]"
  - "[[Cache Invalidation]]"
  - "[[Distributed Cache]]"
tags: []
---

# Caching

## Краткое определение области

`Caching` — это обзорная заметка про использование кэша в распределенных системах как механизма снижения latency, разгрузки источника истины и управления trade-offs между скоростью, свежестью данных и сложностью координации.

## Что входит в эту тему

- `[[Caching Strategies]]`
- `[[Cache Invalidation]]`
- `[[Distributed Cache]]`
- `[[Cache Stampede]]`

## Как устроена ветка

- `Caching Strategies` собирает operational patterns чтения и записи через кэш, чтобы стратегии не смешивались с остальными concept-notes.
- `Cache Invalidation` раскрывает главную conceptual difficulty кэша: как сохранять полезность данных без неконтролируемого устаревания.
- `Distributed Cache` показывает, как кэш перестает быть локальной оптимизацией и становится частью распределенной архитектуры.
- `Cache Stampede` фиксирует типичную failure/performance pathology, возникающую вокруг popular keys и массовых промахов.

## Рекомендуемый маршрут чтения

1. Начать с `[[Caching Strategies]]`, чтобы увидеть базовые модели чтения и записи через кэш.
2. Затем перейти к `[[Cache Invalidation]]`.
3. После этого читать `[[Distributed Cache]]`.
4. Завершить `[[Cache Stampede]]` как типичным failure mode caching-ветки.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Telemetry]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Eviction Policy` и `TTL`
- [ ] Решить, когда нужен отдельный article про `CDN`
- [ ] Проверить `related`
