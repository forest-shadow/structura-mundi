---
aliases:
  - Server-Side Application
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

# Server Application

## Краткое определение

`Server Application` - это программная реализация серверной роли: приложение или сервис, который предоставляет удаленным клиентам доступ к данным, функциям или вычислительным операциям.

## Основная идея или механизм

Серверное приложение не обязано совпадать с одним долгоживущим процессом. Оно может быть реализовано как один процесс, набор worker-процессов, связка proxy plus application, контейнеризированный сервис или serverless runtime.

## Границы темы

- `Server Application` не тождественно `[[Server Process]]`: приложение может исполняться разными процессами и deployment-моделями.
- `Server Application` не тождественно `[[Server Host]]`: машина только размещает реализацию.

## Связи с другими заметками

Родительская тема:

`[[Server]]`

Связанные заметки:

- `[[Server Process]]`
- `[[Service Endpoint]]`

## Примеры, случаи или следствия

HTTP API, gRPC service и custom TCP service можно понимать как разные виды server application, даже если они по-разному устроены на уровне процессов и runtime.
