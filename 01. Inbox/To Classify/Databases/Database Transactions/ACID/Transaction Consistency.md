---
aliases: []
note_type: article
area: computer-science
domain: databases
section: transactions
parent: "[[ACID]]"
status: draft
related:
  - "[[ACID]]"
  - "[[Database Transactions]]"
  - "[[Transaction Isolation]]"
tags:
  - transactions
  - consistency
---

# Transaction Consistency

## Краткое определение

Свойство транзакции, по которому она переводит систему из одного допустимого состояния в другое, не нарушая заданных инвариантов.

## Основная идея или механизм

Transaction consistency относится к сохранению ограничений схемы и предметных правил внутри транзакционной модели. Это не то же самое, что consistency в CAP или в моделях распределённой согласованности.

## Границы темы

- В тему входят schema constraints, referential integrity и бизнес-инварианты, проверяемые в момент фиксации.
- В тему не входят распределённые модели чтения последнего значения и репликационная согласованность.

## Связи с другими заметками

Родительская тема:

`[[ACID]]`

Связанные заметки:

- `[[Database Transactions]]`
- `[[Transaction Isolation]]`

## Примеры, случаи или следствия

Если после перевода суммарный баланс или ссылочная целостность нарушены, транзакция не должна считаться корректной даже при успешном commit.

## Что стоит раскрыть дальше

- [ ] Добавить различие между transaction consistency и CAP-consistency
- [ ] Уточнить роль базы данных и прикладного кода
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
