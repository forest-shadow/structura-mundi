---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Messaging and Coordination Models]]"
status: draft
related:
  - "[[Messaging and Coordination Models]]"
  - "[[Message Broker]]"
  - "[[Publish-Subscribe]]"
tags: []
---

# Brokered Messaging Model

## Краткое определение

`Brokered Messaging Model` - это модель взаимодействия, в которой производители и потребители сообщений обмениваются данными не напрямую, а через посреднический компонент или инфраструктурный слой.

## Основная идея или механизм

Брокер берет на себя прием, буферизацию, маршрутизацию, fan-out или delivery coordination, благодаря чему участники системы могут быть сильнее развязаны по времени и адресации.

## Границы темы

- Это не то же самое, что сам `[[Message Broker]]` как компонент.
- Это не тождественно `[[Publish-Subscribe]]`, потому что brokered messaging может включать и queue-based point-to-point delivery.

## Связи с другими заметками

Родительская тема:

`[[Messaging and Coordination Models]]`

Связанные заметки:

- `[[Message Broker]]`
- `[[Publish-Subscribe]]`

## Примеры, случаи или следствия

Системы очередей, message buses и event brokers удобно описывать сначала как brokered messaging model, а уже затем переходить к их конкретным delivery semantics.
