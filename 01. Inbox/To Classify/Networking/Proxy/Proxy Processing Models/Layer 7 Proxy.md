---
aliases:
  - L7 Proxy
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Processing Models]]"
status: seed
related:
  - "[[Proxy Processing Models]]"
  - "[[Application-Level Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[Reverse Proxy]]"
  - "[[Application Layer Protocols]]"
tags: []
---

# Layer 7 Proxy

## Краткое определение

`Layer 7 Proxy` — это прокси, который принимает решения на уровне application-layer semantics, а не только по connection metadata.

## Основная идея или механизм

L7 proxy понимает структуру прикладного протокола и может применять routing, policy, filtering и transformations на основе application messages. В web-сценариях это особенно часто связано с HTTP-aware reverse proxying.

## Границы темы

- Входит: application-aware proxying и message-aware routing.
- Не входит: purely transport-oriented mediation; это уже `Layer 4 Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Processing Models]]`

Связанные заметки:

- `[[Application-Level Proxy]]`
- `[[HTTP Proxy]]`
- `[[Reverse Proxy]]`
- `[[Application Layer Protocols]]`

## Примеры, случаи или следствия

- L7 proxy может маршрутизировать HTTP traffic по host, path или headers.
- Более глубокая интерпретация трафика дает richer control, но делает прокси более протокол-зависимым.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `Layer 7 Proxy`, `API Gateway` и `Reverse Proxy`
- [ ] Проверить `related`
