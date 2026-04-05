---
aliases:
  - Quick UDP Internet Connections
note_type: article
area: computer-science
domain: networking
section: network-protocols
parent: "[[Transport Layer Protocols]]"
status: seed
related:
  - "[[Transport Layer Protocols]]"
  - "[[HTTP Versions]]"
  - "[[TLS]]"
  - "[[TCP IP Transport Layer]]"
tags: []
---

# QUIC

## Краткое определение

`QUIC` — это современный транспортный протокол поверх UDP, который объединяет установление соединения, криптографическое согласование, multiplexing потоков и механизмы восстановления потерь в единую transport-level модель.

## Основная идея или механизм

Нужно раскрыть, как QUIC переносит transport logic в userspace-протокол поверх UDP, устраняет transport-level head-of-line blocking между независимыми потоками и тесно связывает transport establishment с семантикой TLS 1.3.

## Границы темы

- Входит: transport semantics, stream multiplexing, connection establishment, loss recovery, connection migration.
- Не входит: весь `HTTP/3` как прикладной протокол; это соседняя application-level тема.

## Связи с другими заметками

Родительская тема:

`[[Transport Layer Protocols]]`

Связанные заметки:

- `[[HTTP Versions]]`
- `[[TLS]]`
- `[[TCP IP Transport Layer]]`

## Примеры, случаи или следствия

Добавить 1-3 примера, где QUIC уменьшает latency setup, меняет поведение при packet loss и позволяет HTTP/3 избежать transport-level HOL blocking, характерного для HTTP/2 over TCP.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи с `HTTP/3` и transport-level comparisons
- [ ] Проверить `aliases`
- [ ] Проверить `related`
- [ ] Проверить `tags`
