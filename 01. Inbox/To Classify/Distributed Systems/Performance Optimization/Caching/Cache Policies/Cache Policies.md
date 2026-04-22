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
  - "[[Eviction Policies]]"
  - "[[Expiration Policies]]"
  - "[[Admission Policies]]"
tags: []
---

# Cache Policies

## Краткое определение области

`Cache Policies` — это обзорная заметка про правила, по которым кэш решает, что хранить, как долго хранить и что вытеснять при ограниченных ресурсах.

## Что входит в эту тему

- `[[Eviction Policies]]`
- `[[Expiration Policies]]`
- `[[Admission Policies]]`

## Как устроена ветка

- `Eviction Policies` собирает правила вытеснения объектов при нехватке места.
- `Expiration Policies` описывает правила протухания и freshness windows.
- `Admission Policies` отвечает за то, что вообще стоит допускать в кэш.

## Рекомендуемый маршрут чтения

1. Начать с `[[Eviction Policies]]`.
2. Затем перейти к `[[Expiration Policies]]`.
3. После этого читать `[[Admission Policies]]`.

## Соседние overview-ветки

- `[[Caching]]`
- `[[Cache Invalidation]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `TinyLFU`
- [ ] Проверить `related`
