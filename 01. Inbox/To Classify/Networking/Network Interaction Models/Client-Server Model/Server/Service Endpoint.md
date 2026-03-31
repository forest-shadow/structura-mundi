---
aliases:
  - Service Entry Point
  - Network Endpoint
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Server]]"
status: draft
related:
  - "[[Server]]"
  - "[[Server Process]]"
  - "[[DNS]]"
  - "[[IP Addressing]]"
tags: []
---

# Service Endpoint

## Краткое определение

`Service Endpoint` - это адресуемая сетевая точка входа сервиса: имя, адрес, порт или иной идентификатор, по которому клиент может обратиться к серверной функциональности.

## Основная идея или механизм

Endpoint не является самим сервером. Это сетевая проекция сервиса наружу, через которую клиенты находят и достигают серверную реализацию.

## Границы темы

- `Service Endpoint` не равен `[[Server Host]]`.
- `Service Endpoint` не равен `[[Server Application]]`.

## Связи с другими заметками

Родительская тема:

`[[Server]]`

Связанные заметки:

- `[[DNS]]`
- `[[IP Addressing]]`
- `[[Server Process]]`

## Примеры, случаи или следствия

В web-системах endpoint часто выражается как DNS-имя и порт; в service mesh или RPC-средах он может быть представлен логическим именем сервиса и политиками маршрутизации.
