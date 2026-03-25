---
aliases:
  - Thundering Herd on Cache Miss
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Caching]]"
status: seed
related:
  - "[[Caching]]"
  - "[[Distributed Cache]]"
  - "[[Cache Invalidation]]"
  - "[[Stale-While-Revalidate]]"
tags: []
---

# Cache Stampede

## Краткое определение

`Cache Stampede` — это статья о ситуации, когда множество запросов одновременно промахиваются по одному и тому же ключу и создают всплеск нагрузки на source of truth.

## Границы темы

- Входит: stampede как типовая failure/performance pathology caching systems.
- Не входит: общий разбор всех видов load spikes вне контекста cache behavior.

## Связи с другими заметками

Родительская тема:

`[[Caching]]`

Связанные заметки:

- `[[Distributed Cache]]`
- `[[Cache Invalidation]]`
- `[[Stale-While-Revalidate]]`
- `[[Telemetry]]`

## Примеры, случаи или следствия

- Popular key с истекшим TTL может вызвать synchronized miss storm.
- Кэш, задуманный как защитный буфер, в такой ситуации сам становится триггером деградации всей системы.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про request coalescing и stale-while-revalidate
- [ ] Проверить `related`
