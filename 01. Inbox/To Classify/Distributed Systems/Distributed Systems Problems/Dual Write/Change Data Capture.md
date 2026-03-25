---
aliases:
  - CDC
  - Захват изменений данных
note_type: article
area: computer-science
domain: distributed-systems
section: dual-write
parent: "[[Dual Write]]"
status: seed
related:
  - "[[Transactional Outbox]]"
  - "[[Polling Publisher]]"
tags: []
---

# Change Data Capture

## Краткое определение

Change Data Capture - это подход, при котором изменения в базе данных считываются из журнала транзакций или другого механизма репликации и затем превращаются во внешние события.

## Основная идея или механизм

Нужно раскрыть, как CDC помогает отделить бизнес-запись от публикации события и снизить риск потери сообщения при dual write.

## Границы темы

- Что относится к CDC в контексте dual write.
- Чем CDC отличается от polling publisher.

## Связи с другими заметками

Родительская тема:

`[[Dual Write]]`

Связанные заметки:

- `[[Transactional Outbox]]`
- `[[Polling Publisher]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария чтения change log и публикации событий наружу.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
