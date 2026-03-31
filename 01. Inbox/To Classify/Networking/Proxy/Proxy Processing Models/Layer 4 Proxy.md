---
aliases:
  - L4 Proxy
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Processing Models]]"
status: seed
related:
  - "[[Proxy Processing Models]]"
  - "[[Circuit-Level Proxy]]"
  - "[[Transport Layer Protocols]]"
tags: []
---

# Layer 4 Proxy

## Краткое определение

`Layer 4 Proxy` — это прокси, который принимает решения в основном на уровне transport-layer соединения, адресов и портов, без глубокой интерпретации application semantics.

## Основная идея или механизм

Такой прокси работает на уровне TCP/UDP-like traffic handling и обычно опирается на connection metadata, а не на содержимое прикладных сообщений. Это делает его удобным для более общего и быстрого traffic mediation.

## Границы темы

- Входит: transport-oriented proxying.
- Не входит: глубокий анализ и переписывание application messages; это ближе к `Layer 7 Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Processing Models]]`

Связанные заметки:

- `[[Circuit-Level Proxy]]`
- `[[Transport Layer Protocols]]`

## Примеры, случаи или следствия

- L4 proxy может маршрутизировать соединения по IP, порту и connection metadata.
- Такой прокси обычно универсальнее по отношению к приложению, но слабее понимает его semantics.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `Layer 4 Proxy` и `Load Balancer`
- [ ] Проверить `related`
