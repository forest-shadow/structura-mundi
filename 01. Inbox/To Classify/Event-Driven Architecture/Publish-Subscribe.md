---
aliases:
  - Pub/Sub
  - Публикация-подписка
note_type: article
area: computer-science
domain: distributed-systems
section: event-driven-architecture
parent: "[[Event-Driven Architecture]]"
status: seed
related:
  - "[[Message Broker]]"
  - "[[Event Notification]]"
tags: []
---

# Publish-Subscribe

## Краткое определение

Publish-Subscribe - это паттерн доставки сообщений, при котором издатель не адресует сообщение конкретному получателю, а подписчики получают его по подписке на тему или поток.

## Основная идея или механизм

Нужно раскрыть, как pub/sub уменьшает прямую связность между сервисами и как он поддерживает событийное взаимодействие.

## Границы темы

- Что относится к pub/sub.
- Чем pub/sub отличается от competing consumers и point-to-point delivery.

## Связи с другими заметками

Родительская тема:

`[[Event-Driven Architecture]]`

Связанные заметки:

- `[[Message Broker]]`
- `[[Event Notification]]`

## Примеры, случаи или следствия

Добавить 1-3 схемы fan-out доставки событий.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
