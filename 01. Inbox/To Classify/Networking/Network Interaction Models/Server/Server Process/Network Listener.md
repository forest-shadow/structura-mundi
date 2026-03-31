---
aliases:
  - Listener
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Server Process]]"
status: draft
related:
  - "[[Server Process]]"
  - "[[Transport Layer Protocols]]"
tags: []
---

# Network Listener

## Краткое определение

`Network Listener` - это механизм, через который серверный процесс принимает входящие соединения, запросы или иные транспортные события.

## Основная идея или механизм

В типичном случае listener bind-ится к адресу и порту, переводится в режим listen и затем принимает новые соединения или сообщения для дальнейшей обработки.

## Границы темы

- Listener - это не весь серверный процесс, а только входная сетевая точка.
- На границе находится `[[Service Endpoint]]`, который описывает адресуемое представление сервиса наружу.

## Связи с другими заметками

Родительская тема:

`[[Server Process]]`

Связанные заметки:

- `[[Transport Layer Protocols]]`
- `[[Service Endpoint]]`

## Примеры, случаи или следствия

В Go HTTP server обычно строится вокруг `net.Listener`; в custom TCP service listener напрямую определяет модель приема соединений.
