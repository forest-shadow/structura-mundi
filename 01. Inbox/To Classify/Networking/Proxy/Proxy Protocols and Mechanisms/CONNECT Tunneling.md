---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Protocols and Mechanisms]]"
status: seed
related:
  - "[[HTTP Proxy]]"
  - "[[Forward Proxy]]"
  - "[[Proxy Protocols and Mechanisms]]"
tags: []
---

# CONNECT Tunneling

## Краткое определение

`CONNECT Tunneling` — это механизм, при котором HTTP proxy устанавливает туннель для последующего обмена трафиком между клиентом и целевым узлом.

## Основная идея или механизм

Вместо обычного application-aware mediation прокси создает транспортный туннель через себя. Это особенно важно для сценариев, где клиенту нужен сквозной обмен поверх HTTP proxy, например при защищенных соединениях.

## Границы темы

- Входит: туннелирование через HTTP proxy с помощью CONNECT semantics.
- Не входит: весь HTTP proxying целиком; это более широкая тема `HTTP Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Protocols and Mechanisms]]`

Связанные заметки:

- `[[HTTP Proxy]]`
- `[[Forward Proxy]]`

## Примеры, случаи или следствия

- HTTP proxy может пропускать дальнейший encrypted traffic через созданный CONNECT tunnel.
- CONNECT изменяет роль прокси: вместо глубокого разбора application messages он может перейти к более tunnel-oriented mediation.

## Что стоит раскрыть дальше

- [ ] Проверить `related`
