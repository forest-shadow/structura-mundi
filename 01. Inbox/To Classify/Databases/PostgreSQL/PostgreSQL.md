---
aliases:
  - Postgres
note_type: overview
area: computer-science
domain: databases
section: postgresql
parent: "[[Databases]]"
status: seed
related:
  - "[[Databases]]"
  - "[[PostgreSQL Architecture]]"
  - "[[PostgreSQL Transaction Isolation]]"
  - "[[Transaction Isolation Levels]]"
tags: []
---

# PostgreSQL

## Краткое определение области

`PostgreSQL` — это section-level overview внутри `databases` для заметок о PostgreSQL как о реляционной СУБД общего назначения: ее архитектуре сервера, транзакционном поведении и product-specific operational semantics.

## Что входит в эту тему

- `[[PostgreSQL Architecture]]`
- `[[PostgreSQL Transaction Isolation]]`

## Как устроена ветка

- `PostgreSQL` собирает product-specific заметки, которые не должны растворяться среди общих database concepts.
- `PostgreSQL Architecture` удерживает системный взгляд на устройство сервера, процессы, память и ключевые подсистемы.
- `PostgreSQL Transaction Isolation` удерживает PostgreSQL-specific чтение общей transactional ветки: как общие уровни изоляции реально интерпретируются в PostgreSQL.
- Общие заметки `[[Database Transactions]]`, `[[Transaction Isolation]]` и `[[Transaction Isolation Levels]]` остаются канонической общей рамкой и не дублируются внутри product-ветки.

## Рекомендуемый маршрут чтения

1. Начать с `[[PostgreSQL Architecture]]`, чтобы увидеть общую системную рамку продукта.
2. Затем перейти к `[[PostgreSQL Transaction Isolation]]`.
3. После этого возвращаться к общей ветке `[[Transaction Isolation Levels]]`, если нужно сравнить PostgreSQL-specific семантику с канонической общей моделью.

## Соседние overview-ветки

- Родительская рамка: `[[Databases]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны notes про MVCC, WAL и vacuum
- [ ] Проверить, как ветка соотносится с общей transactional веткой
- [ ] Проверить `related`