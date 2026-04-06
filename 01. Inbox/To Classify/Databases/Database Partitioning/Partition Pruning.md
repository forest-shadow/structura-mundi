---
aliases: []
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Partition Key]]"
  - "[[Horizontal Partitioning]]"
  - "[[Partitioning Trade-offs]]"
tags: []
---

# Partition Pruning

## Краткое определение

`Partition Pruning` — это механизм, при котором planner или executor исключает нерелевантные partitions из выполнения запроса и обращается только к тем частям данных, которые действительно могут содержать нужные строки.

## Основная идея или механизм

Практическая ценность partitioning часто появляется только тогда, когда система умеет не читать все partitions подряд. Pruning опирается на соответствие между предикатом запроса и логикой partition boundary, поэтому выбор partition key и форма SQL-запросов здесь критически важны.

## Границы темы

- Входит: partition elimination, predicate alignment, planner behavior, влияние параметризованных и выраженных запросов.
- Не входит: сам выбор схемы partitioning; это относится к `[[Partitioning Strategy Selection]]`.

## Связи с другими заметками

Родительская тема:

`[[Database Partitioning]]`

Связанные заметки:

- `[[Partition Key]]`
- `[[Horizontal Partitioning]]`
- `[[Partitioning Trade-offs]]`

## Примеры, случаи или следствия

Если таблица разбита по месяцу и запрос фильтрует данные по диапазону дат, planner может читать только нужные месячные partitions. Если же условие заворачивается в функцию, не совпадает с ключом или вычисляется слишком поздно, pruning может не сработать и partitioning не даст ожидаемого выигрыша.

## Что стоит раскрыть дальше

- [ ] Уточнить разницу между static и runtime pruning
- [ ] Добавить связь с формой предикатов и prepared statements
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
