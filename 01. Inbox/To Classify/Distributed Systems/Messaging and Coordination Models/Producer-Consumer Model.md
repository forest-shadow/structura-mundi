---
aliases:
  - Consumer-Producer Model
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Messaging and Coordination Models]]"
status: draft
related:
  - "[[Messaging and Coordination Models]]"
  - "[[Competing Consumers]]"
tags: []
---

# Producer-Consumer Model

## Краткое определение

`Producer-Consumer Model` - это модель координации, в которой одни участники производят работу, данные или сообщения, а другие независимо потребляют и обрабатывают их.

## Основная идея или механизм

Главный смысл модели - разделить темп производства и темп потребления, обычно через буфер, очередь или иной промежуточный канал.

## Границы темы

- Это более общий coordination pattern, чем просто queue implementation.
- На границе находится `[[Competing Consumers]]`, который уже описывает частный scaling pattern внутри consumption-side.

## Связи с другими заметками

Родительская тема:

`[[Messaging and Coordination Models]]`

Связанные заметки:

- `[[Competing Consumers]]`
- `[[Brokered Messaging Model]]`

## Примеры, случаи или следствия

Очереди задач, stream processing stages и background job systems часто естественно описываются как producer-consumer systems.
