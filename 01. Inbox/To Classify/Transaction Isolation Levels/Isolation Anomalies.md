---
aliases:
  - Аномалии изоляции транзакций
note_type: article
area: computer-science
domain: databases
section: transactions
parent: "[[Transaction Isolation Levels]]"
status: seed
related:
  - "[[Transaction Isolation Levels]]"
  - "[[Read Uncommitted]]"
  - "[[Read Committed]]"
  - "[[Repeatable Read]]"
  - "[[Serializable]]"
tags:
  - transactions
  - consistency
---

# Isolation Anomalies

## Краткое определение

Каноническая статья для проблем конкурентного доступа, которые используются как ориентир при сравнении уровней изоляции.

## Основная идея или механизм

Нужно раскрыть, какие виды нежелательного взаимодействия между транзакциями существуют и почему разные уровни изоляции блокируют их по-разному.

## Границы темы

- Что считается классической аномалией изоляции.
- Где тема переходит в описание конкретного уровня изоляции.

## Связи с другими заметками

Родительская тема:

`[[Transaction Isolation Levels]]`

Связанные заметки:

- `[[Read Uncommitted]]`
- `[[Read Committed]]`
- `[[Repeatable Read]]`
- `[[Serializable]]`

## Примеры, случаи или следствия

Добавить примеры dirty read, non-repeatable read и phantom read как базовые ориентиры.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
