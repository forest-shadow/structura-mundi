---
aliases:
  - Конкурирующие потребители
note_type: article
area: computer-science
domain: distributed-systems
section: event-driven-architecture
parent: "[[Event Collaboration Patterns]]"
status: seed
related:
  - "[[Message Broker]]"
  - "[[Idempotent Consumer]]"
tags: []
---

# Competing Consumers

## Краткое определение

Competing Consumers - это паттерн, при котором несколько потребителей читают из общего потока или очереди и разделяют нагрузку между собой.

## Основная идея или механизм

Нужно раскрыть, как паттерн помогает масштабировать обработку событий и какие риски возникают для порядка, повторной доставки и идемпотентности.

## Границы темы

- Что относится к competing consumers.
- Чем этот паттерн отличается от простого publish-subscribe.

## Связи с другими заметками

Родительская тема:

`[[Event Collaboration Patterns]]`

Связанные заметки:

- `[[Message Broker]]`
- `[[Idempotent Consumer]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария распараллеливания обработки событий.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
