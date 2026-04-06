---
aliases:
  - PostgreSQL Isolation Levels
  - Transaction Isolation in PostgreSQL
note_type: article
area: computer-science
domain: databases
section: postgresql
parent: "[[PostgreSQL]]"
status: seed
related:
  - "[[PostgreSQL]]"
  - "[[Transaction Isolation]]"
  - "[[Transaction Isolation Levels]]"
  - "[[Read Committed]]"
  - "[[Repeatable Read]]"
  - "[[Serializable]]"
  - "[[Snapshot Isolation]]"
tags: []
---

# PostgreSQL Transaction Isolation

## Краткое определение

`PostgreSQL Transaction Isolation` — это статья о том, как общие уровни изоляции транзакций реализуются и интерпретируются именно в PostgreSQL.

## Основная идея или механизм

PostgreSQL не просто повторяет ANSI-названия уровней изоляции, а реализует их через собственную product-specific модель конкурентности: `Read Uncommitted` фактически сводится к `Read Committed`, `Repeatable Read` опирается на snapshot-based semantics, а `Serializable` достигается через `Serializable Snapshot Isolation`.

## Границы темы

- В тему входят PostgreSQL-specific различия между `Read Committed`, `Repeatable Read` и `Serializable`, а также место `Read Uncommitted` и связь со `Snapshot Isolation`.
- Рядом находится `[[Transaction Isolation Levels]]`, но она описывает общую каноническую шкалу уровней изоляции, а не product-specific поведение конкретной СУБД.

## Связи с другими заметками

Родительская тема:

`[[PostgreSQL]]`

Связанные заметки:

- `[[Transaction Isolation]]`
- `[[Transaction Isolation Levels]]`
- `[[Read Committed]]`
- `[[Repeatable Read]]`
- `[[Serializable]]`
- `[[Snapshot Isolation]]`

## Примеры, случаи или следствия

Эта заметка нужна, чтобы не смешивать общие названия уровней изоляции с фактической семантикой PostgreSQL: одинаковые labels не гарантируют одинаковое поведение между СУБД.

## Что стоит раскрыть дальше

- [ ] Уточнить роль `Read Uncommitted` как alias-level semantics в PostgreSQL
- [ ] Развести `Repeatable Read`, `Snapshot Isolation` и `Serializable Snapshot Isolation`
- [ ] Проверить, когда рядом нужна отдельная note про PostgreSQL MVCC
- [ ] Проверить `related`
- [ ] Проверить `aliases`