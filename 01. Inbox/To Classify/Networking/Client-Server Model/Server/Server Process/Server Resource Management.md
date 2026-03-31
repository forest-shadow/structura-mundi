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
  - "[[Connection Pooling]]"
  - "[[Go Memory Management]]"
tags: []
---

# Server Resource Management

## Краткое определение

`Server Resource Management` - это управление ограниченными ресурсами серверного процесса: соединениями, памятью, file descriptors, CPU time, очередями работы и другими runtime budgets.

## Основная идея или механизм

Высоконагруженный сервер устойчив не тогда, когда ресурсов "много", а тогда, когда их использование измеримо, ограничено и связано с admission control, pooling и cancellation.

## Границы темы

- Это шире, чем memory management и шире, чем только connection pools.
- На границе находится `[[Server Concurrency Model]]`, потому что уровень параллелизма прямо влияет на давление на ресурсы.

## Связи с другими заметками

Родительская тема:

`[[Server Process]]`

Связанные заметки:

- `[[Connection Pooling]]`
- `[[Server Concurrency Model]]`
- `[[Go Memory Management]]`

## Примеры, случаи или следствия

Ограничения на число соединений, размеры очередей, memory pressure и file descriptor exhaustion часто определяют реальные пределы throughput раньше, чем чистая вычислительная мощность.
