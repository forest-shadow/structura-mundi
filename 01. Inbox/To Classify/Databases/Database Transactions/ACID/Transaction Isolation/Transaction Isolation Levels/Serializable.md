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
  - "[[Repeatable Read]]"
  - "[[Snapshot Isolation]]"
tags:
  - transactions
  - consistency
---

# Serializable

## Краткое определение

Каноническая статья для самого сильного классического уровня изоляции, стремящегося к эквивалентности последовательному выполнению транзакций.

## Основная идея или механизм

Нужно раскрыть, что означает сериализуемость, какие гарантии она дает и какой ценой обычно достигается.

## Границы темы

- Что именно считается сериализуемым исполнением.
- Чем `Serializable` отличается от практических компромиссных моделей вроде `Snapshot Isolation`.

## Связи с другими заметками

Родительская тема:

`[[Transaction Isolation Levels]]`

Связанные заметки:

- `[[Isolation Anomalies]]`
- `[[Repeatable Read]]`
- `[[Snapshot Isolation]]`

## Примеры, случаи или следствия

Добавить пример, где строгая изоляция снижает риск аномалий, но повышает цену конкуренции.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
