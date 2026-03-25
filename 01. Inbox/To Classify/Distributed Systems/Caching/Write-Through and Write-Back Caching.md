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
  - "[[Cache Invalidation]]"
  - "[[Cache-Aside Strategy]]"
  - "[[Distributed Cache]]"
tags: []
---

# Write-Through and Write-Back Caching

## Краткое определение

`Write-Through and Write-Back Caching` — это статья о стратегиях записи через кэш и их различиях по latency, durability risk и consistency behavior.

## Границы темы

- Входит: write-path strategies для cache-integrated systems.
- Не входит: локальные hardware cache policies вне контекста distributed/application caching.

## Связи с другими заметками

Родительская тема:

`[[Caching Strategies]]`

Связанные заметки:

- `[[Cache Invalidation]]`
- `[[Cache-Aside Strategy]]`
- `[[Write-Around Caching]]`
- `[[Distributed Cache]]`

## Примеры, случаи или следствия

- Write-through делает cache and store update более прямолинейными, но увеличивает write latency.
- Write-back снижает latency на write path, но повышает требования к надежности и восстановлению.

## Что стоит раскрыть дальше

- [ ] Решить, когда стоит разделить `Write-Through` и `Write-Back` на отдельные articles
- [ ] Проверить `related`
