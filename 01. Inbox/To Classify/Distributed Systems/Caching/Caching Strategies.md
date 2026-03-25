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
  - "[[Write-Through and Write-Back Caching]]"
  - "[[Cache Invalidation]]"
tags: []
---

# Caching Strategies

## Краткое определение области

`Caching Strategies` — это обзорная заметка про основные operational patterns работы с кэшем: как система читает через кэш, как пишет через кэш и какие trade-offs при этом принимает.

## Что входит в эту тему

- `[[Cache-Aside Strategy]]`
- `[[Write-Through and Write-Back Caching]]`

## Как устроена ветка

- `Cache-Aside Strategy` описывает наиболее распространённый read-path pattern, где приложение само управляет cache miss и последующим populate.
- `Write-Through and Write-Back Caching` собирает write-path strategies и показывает, как меняются latency, durability risk и consistency behavior.

## Рекомендуемый маршрут чтения

1. Начать с `[[Cache-Aside Strategy]]` как с базовой модели чтения через кэш.
2. Затем перейти к `[[Write-Through and Write-Back Caching]]`, чтобы увидеть, как caching меняет write path.
3. После этого вернуться к `[[Cache Invalidation]]`, чтобы связать стратегии с freshness и consistency.

## Соседние overview-ветки

- `[[Caching]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Write-Around Caching`
- [ ] Решить, когда нужны notes про `Read-Through` и `Refresh-Ahead`
- [ ] Проверить `related`
