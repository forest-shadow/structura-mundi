---
aliases:
  - Pub/Sub
  - Публикация-подписка
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Messaging and Coordination Models]]"
status: seed
related:
  - "[[Messaging and Coordination Models]]"
  - "[[Event-Driven Architecture]]"
  - "[[Message Broker]]"
  - "[[Event Notification]]"
tags: []
---

# Publish-Subscribe

## Краткое определение

Publish-Subscribe - это модель доставки сообщений, при которой издатель не адресует сообщение конкретному получателю, а подписчики получают его по подписке на тему, канал или поток.

## Основная идея или механизм

Pub/sub уменьшает прямую связность между участниками и позволяет одному факту или сообщению инициировать fan-out доставку множеству независимых потребителей.

## Границы темы

- Это более общая distributed interaction model, чем просто одна техника внутри EDA.
- На границе находятся `[[Brokered Messaging Model]]`, `[[Event-Driven Architecture]]` и queue-oriented point-to-point delivery.

## Связи с другими заметками

Родительская тема:

`[[Messaging and Coordination Models]]`

Связанные заметки:

- `[[Message Broker]]`
- `[[Event Notification]]`
- `[[Event-Driven Architecture]]`

## Примеры, случаи или следствия

Pub/sub удобно использовать там, где один producer должен публиковать данные или события сразу нескольким независимым consumers без явного знания друг о друге.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между brokered и brokerless pub/sub.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
