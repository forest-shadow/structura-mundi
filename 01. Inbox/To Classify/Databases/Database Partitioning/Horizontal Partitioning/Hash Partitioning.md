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
  - "[[Partitioning Strategy Selection]]"
  - "[[Partitioning Trade-offs]]"
tags: []
---

# Hash Partitioning

## Краткое определение

`Hash Partitioning` — это горизонтальное разбиение, при котором строка попадает в partition на основе hash-функции от partition key.

## Основная идея или механизм

Главное достоинство hash strategy — более равномерное распределение строк и нагрузки при условии, что ключ имеет хорошую кардинальность и не слишком перекошен. Такая схема обычно выигрывает в point lookups и write distribution, но хуже подходит для range scans и time-based lifecycle management.

## Границы темы

- Входит: балансировка данных, равномерность записи, key-based routing.
- Не входит: естественное обслуживание диапазонов по времени или идентификатору; это сильнее выражено в `[[Range Partitioning]]`.

## Связи с другими заметками

Родительская тема:

`[[Horizontal Partitioning]]`

Связанные заметки:

- `[[Partition Key]]`
- `[[Partitioning Strategy Selection]]`
- `[[Partitioning Trade-offs]]`

## Примеры, случаи или следствия

Если большинство запросов обращается по `user_id` или `tenant_id`, hash partitioning помогает избежать концентрации данных в одной области ключевого пространства. Но запросы вида "все события за последние 7 дней" могут потребовать fan-out по многим partitions.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между cardinality и quality of distribution
- [ ] Добавить сценарии для tenant-based workloads
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
