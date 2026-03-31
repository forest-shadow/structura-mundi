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
  - "[[Go Concurrency Model]]"
tags: []
---

# Server Concurrency Model

## Краткое определение

`Server Concurrency Model` - это способ, которым серверный процесс распределяет и координирует одновременную обработку множества соединений, запросов и фоновых задач.

## Основная идея или механизм

Сюда входят event loops, thread-per-connection, worker pools, goroutines, admission control, backpressure и ограничения на параллелизм.

## Границы темы

- Это не общая тема конкурентности как таковой, а ее server-side operational применение.
- На границе находится `[[Server Resource Management]]`, где concurrency влияет уже на стоимость ресурсов.

## Связи с другими заметками

Родительская тема:

`[[Server Process]]`

Связанные заметки:

- `[[Request Handling]]`
- `[[Server Resource Management]]`
- `[[Go Concurrency Model]]`

## Примеры, случаи или следствия

Даже при одинаковом протоколе разные concurrency models могут радикально менять latency, throughput, tail behavior и устойчивость сервиса под нагрузкой.
