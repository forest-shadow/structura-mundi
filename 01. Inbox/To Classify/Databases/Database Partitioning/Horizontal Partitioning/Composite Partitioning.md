---
aliases: []
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Horizontal Partitioning]]"
status: seed
related:
  - "[[Range Partitioning]]"
  - "[[Hash Partitioning]]"
  - "[[Partitioning Strategy Selection]]"
tags: []
---

# Composite Partitioning

## Краткое определение

`Composite Partitioning` — это стратегия, в которой несколько схем partitioning сочетаются последовательно, например `range + hash` или `list + hash`.

## Основная идея или механизм

Composite strategy нужна тогда, когда одна схема хорошо решает только часть задачи. Например, `range` может давать удобный lifecycle и pruning, а добавочный `hash` внутри диапазона помогает убрать hotspot и выровнять нагрузку между внутренними subpartitions.

## Границы темы

- Входит: multi-level partitioning, subpartitioning, комбинирование lifecycle и balance goals.
- Не входит: простое использование одной схемы без дополнительного слоя.

## Связи с другими заметками

Родительская тема:

`[[Horizontal Partitioning]]`

Связанные заметки:

- `[[Range Partitioning]]`
- `[[Hash Partitioning]]`
- `[[Partitioning Strategy Selection]]`

## Примеры, случаи или следствия

Таблицу событий можно сначала делить по месяцу, а затем внутри каждого месяца распределять строки по hash от `tenant_id`. Так система получает и удобный retention lifecycle, и лучшее распределение write load, но платит дополнительной сложностью схемы и эксплуатации.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между composite partitioning и просто сложной схемой routing
- [ ] Добавить случаи `range + hash` и `list + hash`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
