---
aliases:
  - Транзакционный аутбокс
note_type: article
area: computer-science
domain: distributed-systems
section: event-driven-architecture
parent: "[[Event-Driven Architecture]]"
status: seed
related:
  - "[[Idempotent Consumer]]"
  - "[[Message Broker]]"
tags: []
---

# Transactional Outbox

## Краткое определение

Transactional Outbox - это паттерн, в котором событие сначала записывается вместе с изменением бизнес-состояния в локальное хранилище, а затем публикуется асинхронно.

## Основная идея или механизм

Нужно раскрыть, как outbox помогает согласовать изменение данных и публикацию события без распределенной транзакции.

## Границы темы

- Что относится к transactional outbox.
- Чем этот паттерн отличается от прямой публикации в брокер внутри бизнес-транзакции.

## Связи с другими заметками

Родительская тема:

`[[Event-Driven Architecture]]`

Связанные заметки:

- `[[Idempotent Consumer]]`
- `[[Message Broker]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария публикации событий после commit.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
