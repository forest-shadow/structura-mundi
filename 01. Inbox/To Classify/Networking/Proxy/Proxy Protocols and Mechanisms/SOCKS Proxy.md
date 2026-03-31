---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Protocols and Mechanisms]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Forward Proxy]]"
  - "[[Circuit-Level Proxy]]"
  - "[[Explicit Proxy]]"
tags: []
---

# SOCKS Proxy

## Краткое определение

`SOCKS Proxy` — это прокси, который посредничает на уровне более общего connection/tunneling behavior и не ограничен одной HTTP-specific semantics.

## Основная идея или механизм

SOCKS выступает как универсальный proxy-mechanism для перенаправления клиентских соединений через посредника. Он обычно ближе к circuit-level mediation, чем к rich application-aware processing.

## Границы темы

- Входит: SOCKS-based proxying и connection-oriented tunneling behavior.
- Не входит: HTTP-specific message semantics; это уже ближе к `HTTP Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Protocols and Mechanisms]]`

Связанные заметки:

- `[[Forward Proxy]]`
- `[[Circuit-Level Proxy]]`
- `[[Explicit Proxy]]`

## Примеры, случаи или следствия

- Клиент может использовать SOCKS proxy как универсальный outbound intermediary.
- SOCKS подходит там, где нужна более general connection mediation, а не HTTP-aware routing.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли отдельный article про `SOCKS5`
- [ ] Проверить `related`
