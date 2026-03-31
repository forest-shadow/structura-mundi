---
aliases:
  - Server Machine
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Server]]"
status: draft
related:
  - "[[Server]]"
  - "[[Server Process]]"
  - "[[Service Endpoint]]"
tags: []
---

# Server Host

## Краткое определение

`Server Host` - это машина, виртуальный узел или execution environment, на котором размещается серверный процесс или сервис.

## Основная идея или механизм

В повседневной речи словом `server` часто называют именно хост, но это вторичное употребление. Хост предоставляет вычислительные ресурсы и сетевое присутствие, но сам по себе не исчерпывает понятие сервера как роли или приложения.

## Границы темы

- `Server Host` не равен `[[Server Process]]`.
- `Server Host` не равен `[[Service Endpoint]]`.

## Связи с другими заметками

Родительская тема:

`[[Server]]`

Связанные заметки:

- `[[Server Process]]`
- `[[Service Endpoint]]`

## Примеры, случаи или следствия

Один хост может обслуживать несколько серверных процессов, а один логический сервис может быть распределен по множеству хостов.
