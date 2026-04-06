---
aliases:
  - Horizontal Database Partitioning
note_type: overview
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Vertical Partitioning]]"
  - "[[Partition Key]]"
  - "[[Sharding]]"
tags: []
---

# Horizontal Partitioning

## Краткое определение области

`Horizontal Partitioning` — это обзорная заметка о разбиении данных по строкам, когда каждая partition хранит свой поднабор записей, но сохраняет ту же самую схему таблицы.

## Что входит в эту тему

- `[[Range Partitioning]]`
- `[[Hash Partitioning]]`
- `[[List Partitioning]]`
- `[[Composite Partitioning]]`

## Как устроена ветка

- `Range Partitioning` подходит там, где данные естественно упорядочены по времени, идентификатору или иному линейному признаку.
- `Hash Partitioning` помогает равномернее размазывать нагрузку, если для системы важнее баланс записи и point lookups, чем range scans.
- `List Partitioning` полезен, когда набор категорий заранее ограничен и семантически стабилен.
- `Composite Partitioning` нужен, когда одной стратегии недостаточно и приходится сочетать, например, range для lifecycle и hash для balance.

## Рекомендуемый маршрут чтения

1. Начать с `[[Range Partitioning]]` как наиболее интуитивного сценария.
2. Затем сравнить его с `[[Hash Partitioning]]` и `[[List Partitioning]]`.
3. После этого перейти к `[[Composite Partitioning]]` как к способу сочетать несколько критериев.

## Соседние overview-ветки

- Родительская рамка: `[[Database Partitioning]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный note про subpartitioning
- [ ] Проверить, когда `Horizontal Partitioning` требует product-specific продолжения
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
