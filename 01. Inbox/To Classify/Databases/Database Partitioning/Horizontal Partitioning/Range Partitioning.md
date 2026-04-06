---
aliases: []
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Horizontal Partitioning]]"
status: seed
related:
  - "[[Partition Key]]"
  - "[[Partition Pruning]]"
  - "[[Partitioning Strategy Selection]]"
tags: []
---

# Range Partitioning

## Краткое определение

`Range Partitioning` — это горизонтальное разбиение, при котором каждая partition отвечает за определенный диапазон значений partition key.

## Основная идея или механизм

Такая стратегия особенно естественна для временных рядов, журналов событий, batch-данных и вообще для случаев, где данные приходят в упорядоченной последовательности. Она хорошо сочетается с retention policies, archival workflows и range predicates.

## Границы темы

- Входит: time-based partitioning, id-based ranges, lifecycle-driven partitions.
- Не входит: равномерное распределение нагрузки без опоры на естественный порядок ключа; это ближе к `[[Hash Partitioning]]`.

## Связи с другими заметками

Родительская тема:

`[[Horizontal Partitioning]]`

Связанные заметки:

- `[[Partition Key]]`
- `[[Partition Pruning]]`
- `[[Partitioning Strategy Selection]]`

## Примеры, случаи или следствия

Таблицу логов можно делить по месяцу или дню. Тогда старые partitions легко архивировать или удалять целиком, а запросы по диапазону дат хорошо сочетаются с pruning. Основная цена такого подхода — риск горячей последней partition при монотонно растущем ключе.

## Что стоит раскрыть дальше

- [ ] Добавить сценарии для retention-heavy workloads
- [ ] Уточнить риск hotspot на последних диапазонах
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
