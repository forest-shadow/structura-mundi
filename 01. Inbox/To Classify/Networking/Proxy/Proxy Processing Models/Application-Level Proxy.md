---
aliases:
  - Application Proxy
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Processing Models]]"
status: seed
related:
  - "[[Proxy Processing Models]]"
  - "[[HTTP Proxy]]"
  - "[[Layer 7 Proxy]]"
  - "[[Application Layer Protocols]]"
tags: []
---

# Application-Level Proxy

## Краткое определение

`Application-Level Proxy` — это прокси, который понимает semantics прикладного протокола и работает не только с соединением, но и с содержательной структурой application messages.

## Основная идея или механизм

Такой прокси способен интерпретировать запросы и ответы как сущности прикладного уровня, применять протокол-специфичные policy и трансформации, а не просто пересылать байты между endpoints.

## Границы темы

- Входит: protocol-aware proxying на уровне application semantics.
- Не входит: чистое connection mediation без разбора application messages; это уже `Circuit-Level Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Processing Models]]`

Связанные заметки:

- `[[HTTP Proxy]]`
- `[[Layer 7 Proxy]]`
- `[[Application Layer Protocols]]`

## Примеры, случаи или следствия

- HTTP-aware proxy может принимать решения на основе методов, заголовков и routing rules.
- Application-level proxying позволяет richer policy enforcement, но требует более глубокого понимания протокола.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `Application-Level Proxy` и `Layer 7 Proxy`
- [ ] Проверить `related`
