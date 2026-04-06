---
aliases: []
note_type: overview
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Databases]]"
status: seed
related:
  - "[[Horizontal Partitioning]]"
  - "[[Vertical Partitioning]]"
  - "[[Partitioning Strategy Selection]]"
  - "[[Sharding]]"
tags: []
---

# Database Partitioning

## Краткое определение области

`Database Partitioning` — это обзорная заметка о способах разбить одну логическую таблицу или набор данных на несколько физических частей так, чтобы упростить масштабирование, обслуживание, маршрутизацию запросов и управление жизненным циклом данных.

## Что входит в эту тему

- `[[Horizontal Partitioning]]`
- `[[Vertical Partitioning]]`
- `[[Partition Key]]`
- `[[Partition Pruning]]`
- `[[Partitioning Trade-offs]]`
- `[[Partitioning Strategy Selection]]`
- `[[Sharding]]`

## Как устроена ветка

- `Horizontal Partitioning` собирает row-based strategies, где данные делятся по строкам и значению ключа.
- `Vertical Partitioning` отвечает за column-based decomposition, когда разные группы колонок уносятся в разные физические структуры.
- `Partition Key` описывает главный инженерный выбор ветки: по какому признаку данные будут размещаться и как по ним будут маршрутизироваться запросы.
- `Partition Pruning` объясняет, откуда берется реальный performance gain и почему partitioning без корректных предикатов может не дать ожидаемого выигрыша.
- `Partitioning Trade-offs` фиксирует издержки, без которых тема была бы описана слишком оптимистично.
- `Partitioning Strategy Selection` отвечает на практический вопрос: в каких ситуациях и как именно стоит применять разные варианты partitioning.
- `Sharding` показывает, как partitioning переходит в distributed deployment на уровне нескольких узлов или инстансов.

## Рекомендуемый маршрут чтения

1. Начать с `[[Partition Key]]`, чтобы понять, по какому признаку вообще делятся данные.
2. Затем пройти `[[Horizontal Partitioning]]` и `[[Vertical Partitioning]]`.
3. После этого перейти к `[[Partition Pruning]]` и `[[Partitioning Trade-offs]]`.
4. Завершить ветку `[[Partitioning Strategy Selection]]` и `[[Sharding]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Databases]]`
- Product-specific продолжение: `[[PostgreSQL]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужен отдельный note про rebalancing partitions
- [ ] Проверить, нужен ли отдельный note про global indexes
- [ ] Проверить, когда product-specific material стоит выносить в `PostgreSQL`
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
