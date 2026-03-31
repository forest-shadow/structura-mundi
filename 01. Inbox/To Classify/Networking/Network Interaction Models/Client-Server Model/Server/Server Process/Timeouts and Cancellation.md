---
aliases: []
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Server Process]]"
status: draft
related:
  - "[[Server Process]]"
  - "[[Request Handling]]"
  - "[[Server Lifecycle Management]]"
tags: []
---

# Timeouts and Cancellation

## Краткое определение

`Timeouts and Cancellation` - это механизмы, которые ограничивают длительность серверной работы и позволяют прерывать обработку, утратившую смысл, budget или полезность.

## Основная идея или механизм

Они защищают сервер от зависающих соединений, бесконечно долгих запросов, resource leaks и неконтролируемого накопления работы.

## Границы темы

- Это не только transport-level timeouts, но и application-level cancellation.
- На границе находится `[[Server Resource Management]]`, потому что таймауты прямо влияют на occupancy ресурсов.

## Связи с другими заметками

Родительская тема:

`[[Server Process]]`

Связанные заметки:

- `[[Request Handling]]`
- `[[Server Resource Management]]`
- `[[Server Lifecycle Management]]`

## Примеры, случаи или следствия

Корректные deadlines и cancellation paths часто важнее raw throughput, потому что они ограничивают tail latency и защищают сервер при partial failure.
