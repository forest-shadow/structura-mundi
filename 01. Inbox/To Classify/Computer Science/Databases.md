---
aliases:
  - Database Systems
note_type: overview
area: computer-science
domain: databases
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Database Transactions]]"
  - "[[ACID]]"
  - "[[Transaction Isolation Levels]]"
  - "[[Redis]]"
tags: []
---

# Databases

## Краткое определение области

`Databases` — это доменная обзорная заметка для веток про организацию, хранение, согласованность и транзакционное поведение данных в управляемых системах хранения.

## Что входит в эту тему

- `[[Database Transactions]]`
- `[[ACID]]`
- `[[Transaction Isolation Levels]]`
- `[[Redis]]`

## Как устроена ветка

- на текущем этапе внутри `Databases` уже видны две разные логики роста: `transactions` как ветка про корректность, изоляцию и семантику фиксации изменений, и `redis` как product-specific ветка про in-memory data structure store;
- `Database Transactions` лучше понимать как первый устойчивый sub-overview внутри domain `databases`, потому что вокруг него уже собран реальный корпус дочерних notes;
- `Redis` можно оформлять как отдельный section-level overview внутри `databases`, потому что рядом с ним естественно возникают заметки о модели данных, типах структур, TTL, persistence и operational trade-offs;
- доменная рамка нужна заранее, чтобы не смешивать database notes напрямую с корневой картой `Computer Science`.

## Рекомендуемый маршрут чтения

1. Начать с `[[Database Transactions]]` как базовой обзорной рамки.
2. Затем перейти к `[[ACID]]` и `[[Transaction Isolation Levels]]`.
3. Для product-specific data structure branch перейти к `[[Redis]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Проверить, что domain-root overview остается без `section`
- [ ] Решить, нужен ли позже отдельный узел для storage engines или query processing
- [ ] Проверить, как ветка `Redis` соотносится с database-internals и distributed-cache темами
- [ ] Решить, когда внутри `Databases` нужны sibling-ветки рядом с `transactions` и `redis`
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
