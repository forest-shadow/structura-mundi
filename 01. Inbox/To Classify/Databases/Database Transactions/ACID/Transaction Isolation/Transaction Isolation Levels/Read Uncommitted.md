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
  - "[[Transaction Isolation Levels]]"
tags:
  - transactions
  - consistency
---

# Read Uncommitted

## Краткое определение

Каноническая статья для самого слабого классического уровня изоляции.

## Основная идея или механизм

Нужно раскрыть, какие чтения он допускает, какие аномалии не предотвращает и почему на практике используется редко или ограниченно.

## Границы темы

- Какие гарантии дает этот уровень.
- Чем он отличается от `Read Committed`.

## Связи с другими заметками

Родительская тема:

`[[Transaction Isolation Levels]]`

Связанные заметки:

- `[[Isolation Anomalies]]`
- `[[Read Committed]]`

## Примеры, случаи или следствия

Добавить пример dirty read и его последствий.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
