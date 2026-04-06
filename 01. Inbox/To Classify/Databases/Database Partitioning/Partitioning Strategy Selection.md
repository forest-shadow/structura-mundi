---
aliases:
  - Database Partitioning Strategy Selection
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Horizontal Partitioning]]"
  - "[[Vertical Partitioning]]"
  - "[[Partition Key]]"
  - "[[Partitioning Trade-offs]]"
  - "[[Sharding]]"
tags: []
---

# Partitioning Strategy Selection

## Краткое определение

`Partitioning Strategy Selection` — это заметка о том, в каких ситуациях partitioning действительно стоит применять и как выбирать подходящую схему разбиения под конкретный workload.

## Основная идея или механизм

Выбор strategy должен исходить не из абстрактной популярности partitioning, а из реальных access patterns, lifecycle данных, требований к maintenance и ограничений инфраструктуры. Хорошая стратегия минимизирует fan-out запросов и перекос нагрузки, а также дает понятный operational выигрыш.

## Границы темы

- Входит: связь между workload и partitioning scheme, критерии выбора, migration concerns, operational constraints.
- Не входит: глубокое описание каждой отдельной техники; это уже темы `[[Horizontal Partitioning]]`, `[[Vertical Partitioning]]` и дочерних notes.

## Связи с другими заметками

Родительская тема:

`[[Database Partitioning]]`

Связанные заметки:

- `[[Horizontal Partitioning]]`
- `[[Vertical Partitioning]]`
- `[[Partition Key]]`
- `[[Partitioning Trade-offs]]`
- `[[Sharding]]`

## Примеры, случаи или следствия

Если главный сценарий — time-series или append-only data с retention windows, чаще всего первым кандидатом будет `[[Range Partitioning]]`. Если система живет на point lookups по tenant/user key и страдает от uneven load, разумнее смотреть в сторону `[[Hash Partitioning]]`. Если partitions должны совпадать с небольшим стабильным набором бизнес-категорий или регионов, подходит `[[List Partitioning]]`. Если single-node limits уже исчерпаны, вопрос может перейти из обычного partitioning в `[[Sharding]]`.

## Что стоит раскрыть дальше

- [ ] Добавить decision framework по типам workload
- [ ] Уточнить, когда partitioning не нужен и только усложняет систему
- [ ] Проверить связь с migration и backfill strategy
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
