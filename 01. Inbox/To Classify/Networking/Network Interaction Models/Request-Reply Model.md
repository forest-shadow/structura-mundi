---
aliases:
  - Request-Response Model
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Network Interaction Models]]"
status: draft
related:
  - "[[Network Interaction Models]]"
  - "[[Client-Server Model]]"
tags: []
---

# Request-Reply Model

## Краткое определение

`Request-Reply Model` - это модель взаимодействия, в которой одна сторона отправляет запрос, а другая возвращает ответ, образуя логически связанную пару сообщений.

## Основная идея или механизм

Эта модель описывает форму обмена, а не конкретную архитектурную роль участников. Поэтому она может реализовываться и в client-server системах, и в иных сетевых или распределенных контекстах.

## Границы темы

- `Request-Reply Model` не тождественна `[[Client-Server Model]]`.
- Здесь важна именно корреляция запроса и ответа, а не fixed deployment roles.

## Связи с другими заметками

Родительская тема:

`[[Network Interaction Models]]`

Связанные заметки:

- `[[Client-Server Model]]`

## Примеры, случаи или следствия

HTTP, RPC и многие application-layer protocols используют request-reply как базовую exchange form, даже если поверх этого строятся более сложные patterns.
