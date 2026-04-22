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
  - "[[Write-Through and Write-Back Caching]]"
  - "[[Cache Invalidation]]"
tags: []
---

# Write-Around Caching

## Краткое определение

`Write-Around Caching` — это статья о стратегии, в которой записи идут напрямую в source of truth, а кэш наполняется позже только по фактическим чтениям.

## Границы темы

- Входит: write-around как write-path strategy для снижения cache pollution.
- Не входит: write-through и write-back как стратегии записи через cache layer.

## Связи с другими заметками

Родительская тема:

`[[Caching Strategies]]`

Связанные заметки:

- `[[Write-Through and Write-Back Caching]]`
- `[[Cache-Aside Strategy]]`
- `[[Cache Invalidation]]`

## Примеры, случаи или следствия

- Write-around полезен, когда не все записи будут потом реально читаться.
- Цена этой стратегии — возможный miss сразу после write.

## Что стоит раскрыть дальше

- [ ] Проверить, когда стоит связать note с workload patterns
- [ ] Проверить `related`
