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
  - "[[HTTP Proxy]]"
  - "[[SOCKS Proxy]]"
  - "[[Proxy Protocols and Mechanisms]]"
tags: []
---

# Proxy Chaining

## Краткое определение

`Proxy Chaining` — это схема, при которой трафик проходит последовательно через несколько proxy-узлов.

## Основная идея или механизм

Вместо одного посредника формируется цепочка intermediaries, где каждый следующий прокси становится downstream-hop для предыдущего. Это важно для layered policy, segmented access и некоторых privacy-oriented deployment patterns.

## Границы темы

- Входит: последовательное прохождение через несколько proxy nodes.
- Не входит: обычный single-proxy deployment.

## Связи с другими заметками

Родительская тема:

`[[Proxy Protocols and Mechanisms]]`

Связанные заметки:

- `[[HTTP Proxy]]`
- `[[SOCKS Proxy]]`

## Примеры, случаи или следствия

- Организация может строить несколько proxy hops для разделения policy domains.
- Каждое дополнительное proxy-звено усложняет trust model, latency profile и диагностику.

## Что стоит раскрыть дальше

- [ ] Проверить `related`
