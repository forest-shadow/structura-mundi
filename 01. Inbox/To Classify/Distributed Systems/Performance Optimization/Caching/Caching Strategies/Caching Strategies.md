---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Caching]]"
status: seed
related:
  - "[[Caching]]"
  - "[[Cache-Aside Strategy]]"
  - "[[Read-Through and Refresh-Ahead Caching]]"
  - "[[Write-Through and Write-Back Caching]]"
  - "[[Write-Around Caching]]"
  - "[[Stale-While-Revalidate]]"
  - "[[Negative Caching]]"
  - "[[Cache Invalidation]]"
tags: []
---

# Caching Strategies

## Краткое определение области

`Caching Strategies` — это обзорная заметка про основные operational patterns работы с кэшем: как система читает через кэш, как пишет через кэш и какие trade-offs при этом принимает.

## Что входит в эту тему

- `[[Cache-Aside Strategy]]`
- `[[Read-Through and Refresh-Ahead Caching]]`
- `[[Write-Through and Write-Back Caching]]`
- `[[Write-Around Caching]]`
- `[[Stale-While-Revalidate]]`
- `[[Negative Caching]]`

## Как устроена ветка

- `Cache-Aside Strategy` описывает наиболее распространённый read-path pattern, где приложение само управляет cache miss и последующим populate.
- `Read-Through and Refresh-Ahead Caching` собирает более "умные" read-oriented patterns на стороне cache layer.
- `Write-Through and Write-Back Caching` собирает основные write-path strategies.
- `Write-Around Caching` дополняет write-path ветку стратегией без немедленного наполнения кэша.
- `Stale-While-Revalidate` фиксирует controlled staleness как отдельный способ управления latency и freshness.
- `Negative Caching` показывает, что кэшировать можно не только positive hits, но и отсутствующие значения.

## Рекомендуемый маршрут чтения

1. Начать с `[[Cache-Aside Strategy]]` как с базовой модели чтения через кэш.
2. Затем перейти к `[[Read-Through and Refresh-Ahead Caching]]`.
3. После этого читать `[[Write-Through and Write-Back Caching]]` и `[[Write-Around Caching]]`.
4. Завершить `[[Stale-While-Revalidate]]` и `[[Negative Caching]]` как специальными operational patterns.

## Соседние overview-ветки

- `[[Caching]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Request Coalescing`
- [ ] Решить, когда нужно разделить `Read-Through` и `Refresh-Ahead`
- [ ] Проверить `related`
