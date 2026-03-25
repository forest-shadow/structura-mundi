---
aliases:
  - Передача состояния через событие
note_type: article
area: computer-science
domain: distributed-systems
section: event-driven-architecture
parent: "[[Event Collaboration Patterns]]"
status: seed
related:
  - "[[Event Notification]]"
  - "[[Competing Consumers]]"
tags: []
---

# Event-Carried State Transfer

## Краткое определение

Event-Carried State Transfer - это паттерн, при котором событие переносит достаточно данных, чтобы потребитель мог обновить свое локальное представление без дополнительного запроса.

## Основная идея или механизм

Нужно раскрыть, как включение состояния в событие снижает связность по синхронным вызовам и какие компромиссы это создает.

## Границы темы

- Что относится именно к event-carried state transfer.
- Чем он отличается от event notification.

## Связи с другими заметками

Родительская тема:

`[[Event Collaboration Patterns]]`

Связанные заметки:

- `[[Event Notification]]`
- `[[Competing Consumers]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария, где потребителю достаточно данных из события.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
