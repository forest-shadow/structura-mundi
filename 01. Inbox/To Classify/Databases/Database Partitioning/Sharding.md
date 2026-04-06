---
aliases:
  - Database Sharding
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Horizontal Partitioning]]"
  - "[[Partition Key]]"
  - "[[Partitioning Trade-offs]]"
tags: []
---

# Sharding

## Краткое определение

`Sharding` — это distributed form горизонтального partitioning, при которой разные части одного логического набора данных размещаются на разных узлах, инстансах или кластерах базы данных.

## Основная идея или механизм

Sharding применяют тогда, когда partitioning уже нужен не только ради удобства локального управления таблицей, но и ради распределения хранения и нагрузки между несколькими вычислительными узлами. Обычно он требует явного shard key, маршрутизации запросов, процедур rebalancing и продуманной стратегии для cross-shard operations.

## Границы темы

- Входит: shard key, routing, rebalancing, cross-shard reads/writes, distributed growth limits.
- Не входит: локальное partitioning внутри одной инстанции без распределения данных по узлам.

## Связи с другими заметками

Родительская тема:

`[[Database Partitioning]]`

Связанные заметки:

- `[[Horizontal Partitioning]]`
- `[[Partition Key]]`
- `[[Partitioning Trade-offs]]`

## Примеры, случаи или следствия

Для multi-tenant SaaS sharding по tenant id может помочь изолировать нагрузку и масштабироваться за пределы одного узла. Но он почти всегда усложняет агрегации, транзакции, глобальные ограничения и эксплуатацию, поэтому переход к нему обычно оправдан только после реального упора в single-node limits.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между sharding и обычным partitioning внутри одной СУБД
- [ ] Добавить сценарии для tenant-based и geography-based sharding
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
