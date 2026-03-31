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
  - "[[Reverse Proxy]]"
  - "[[Layer 7 Proxy]]"
  - "[[HTTP]]"
  - "[[CONNECT Tunneling]]"
tags: []
---

# HTTP Proxy

## Краткое определение

`HTTP Proxy` — это прокси, который работает в HTTP-контексте и использует HTTP semantics для посредничества между сторонами взаимодействия.

## Основная идея или механизм

Такой прокси понимает HTTP requests and responses и может работать либо как client-side proxy, либо как server-side proxy в web-oriented сценариях. Важная особенность темы в том, что она находится на пересечении proxying и HTTP semantics, но не исчерпывает ни одну из этих веток целиком.

## Границы темы

- Входит: HTTP-aware proxying и HTTP-specific mediation mechanisms.
- Не входит: весь HTTP как protocol family; это уже тема `HTTP`.
- Не входит: весь общий класс proxy; это тема `Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Protocols and Mechanisms]]`

Связанные заметки:

- `[[HTTP]]`
- `[[Forward Proxy]]`
- `[[Reverse Proxy]]`
- `[[Layer 7 Proxy]]`
- `[[CONNECT Tunneling]]`

## Примеры, случаи или следствия

- Browser-oriented forward proxy может быть HTTP proxy.
- Многие reverse proxies в web-infrastructure работают как HTTP-aware intermediaries.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `HTTP Proxy`, `Reverse Proxy` и `Layer 7 Proxy`
- [ ] Проверить `related`
