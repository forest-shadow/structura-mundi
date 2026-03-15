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
  - "[[Read Committed]]"
  - "[[Serializable]]"
tags:
  - transactions
  - consistency
---

# Repeatable Read

## Краткое определение

Каноническая статья для уровня изоляции, который усиливает стабильность чтений по сравнению с `Read Committed`.

## Основная идея или механизм

Нужно объяснить, какие аномалии этот уровень предотвращает, какие еще может допускать и как его поведение зависит от конкретной СУБД.

## Границы темы

- Какие гарантии считаются минимально ожидаемыми от `Repeatable Read`.
- Где тема пересекается с `Snapshot Isolation` и `Serializable`.

## Связи с другими заметками

Родительская тема:

`[[Transaction Isolation Levels]]`

Связанные заметки:

- `[[Isolation Anomalies]]`
- `[[Read Committed]]`
- `[[Serializable]]`

## Примеры, случаи или следствия

Добавить пример стабильного повторного чтения и указать, какие эффекты все еще могут оставаться.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
