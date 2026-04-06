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
  - "[[Sharding]]"
tags: []
---

# List Partitioning

## Краткое определение

`List Partitioning` — это горизонтальное разбиение, при котором каждая partition соответствует заранее заданному набору дискретных значений partition key.

## Основная идея или механизм

List strategy полезна там, где бизнес-семантика уже делит данные на небольшое и относительно стабильное число категорий: регионы, типы клиентов, продуктовые линии или группы tenants. Она делает routing понятным и явным, но плохо переносит взрывной рост числа категорий или их частые изменения.

## Границы темы

- Входит: region-based, category-based, bounded-tenant-group partitioning.
- Не входит: автоматическое равномерное распределение по большому ключевому пространству; это уже ближе к `[[Hash Partitioning]]`.

## Связи с другими заметками

Родительская тема:

`[[Horizontal Partitioning]]`

Связанные заметки:

- `[[Partition Key]]`
- `[[Partitioning Strategy Selection]]`
- `[[Sharding]]`

## Примеры, случаи или следствия

Если система хранит данные по фиксированным регионам `EU`, `US` и `APAC`, list partitioning позволяет явно закрепить каждый регион за своей partition. Такой подход удобен для governance и data residency, но со временем может давать сильный skew, если один регион растет быстрее остальных.

## Что стоит раскрыть дальше

- [ ] Добавить связь с region-based routing и data residency
- [ ] Уточнить риски category skew
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
