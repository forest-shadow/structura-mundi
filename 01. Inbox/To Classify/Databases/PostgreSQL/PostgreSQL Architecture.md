---
aliases:
  - Architecture of PostgreSQL
note_type: article
area: computer-science
domain: databases
section: postgresql
parent: "[[PostgreSQL]]"
status: seed
related:
  - "[[PostgreSQL]]"
  - "[[PostgreSQL Transaction Isolation]]"
tags: []
---

# PostgreSQL Architecture

## Краткое определение

`PostgreSQL Architecture` — это статья о том, как устроен PostgreSQL как серверная СУБД: процессы, память, запись изменений, фоновая работа и основные системные подсистемы.

## Основная идея или механизм

Архитектура PostgreSQL важна потому, что product-specific поведение транзакций, конкурентности и устойчивости изменений определяется не только SQL-уровнем, но и внутренним устройством сервера, его процессов и storage-path.

## Границы темы

- В тему входят postmaster/process model, backend processes, shared buffers, WAL, checkpoints и общий архитектурный каркас сервера.
- Рядом находится `[[PostgreSQL Transaction Isolation]]`, но она описывает уже семантику транзакционного поведения, а не общую системную рамку продукта.

## Связи с другими заметками

Родительская тема:

`[[PostgreSQL]]`

Связанные заметки:

- `[[PostgreSQL Transaction Isolation]]`

## Примеры, случаи или следствия

Архитектурная заметка нужна, чтобы product-specific особенности PostgreSQL не воспринимались как чисто SQL-level магия: за ними стоят конкретные процессы, shared state и механизмы записи изменений.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны отдельные notes про WAL, shared buffers и vacuum
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`