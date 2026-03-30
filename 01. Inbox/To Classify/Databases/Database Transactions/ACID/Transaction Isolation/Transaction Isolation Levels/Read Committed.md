---
aliases: []
note_type: article
area: computer-science
domain: databases
section: transactions
parent: "[[Transaction Isolation Levels]]"
status: seed
related:
  - "[[Isolation Anomalies]]"
  - "[[Read Uncommitted]]"
  - "[[Repeatable Read]]"
tags:
  - transactions
  - consistency
---

# Read Committed

## Краткое определение

Каноническая статья для уровня изоляции, который запрещает чтение неподтвержденных данных, но все еще допускает часть аномалий конкурентного доступа.

## Основная идея или механизм

Нужно показать, какие гарантии появляются по сравнению с `Read Uncommitted` и какие проблемы все еще остаются открытыми.

## Границы темы

- Что именно исключается на этом уровне.
- Где начинаются требования к более сильным уровням.

## Связи с другими заметками

Родительская тема:

`[[Transaction Isolation Levels]]`

Связанные заметки:

- `[[Isolation Anomalies]]`
- `[[Read Uncommitted]]`
- `[[Repeatable Read]]`

## Примеры, случаи или следствия

Добавить пример, где dirty read уже исключен, но non-repeatable read еще возможен.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
