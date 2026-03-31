---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Processing Models]]"
status: seed
related:
  - "[[Proxy Processing Models]]"
  - "[[SOCKS Proxy]]"
  - "[[Layer 4 Proxy]]"
tags: []
---

# Circuit-Level Proxy

## Краткое определение

`Circuit-Level Proxy` — это прокси, который посредничает на уровне соединения или session semantics, не анализируя полноценно прикладное содержимое протокола.

## Основная идея или механизм

Такой прокси создает и управляет соединением между сторонами, но обычно не интерпретирует запросы и ответы как rich application messages. Это делает его ближе к tunneling и connection mediation, чем к application-aware proxying.

## Границы темы

- Входит: connection-level mediation и tunnel-oriented proxying.
- Не входит: глубокая обработка semantics HTTP, SMTP и других прикладных протоколов; это уже ближе к `Application-Level Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Processing Models]]`

Связанные заметки:

- `[[SOCKS Proxy]]`
- `[[Layer 4 Proxy]]`

## Примеры, случаи или следствия

- SOCKS-прокси часто рассматривается как пример circuit-level proxying.
- Такой прокси может быть более универсальным, но менее application-aware.

## Что стоит раскрыть дальше

- [ ] Проверить `related`
