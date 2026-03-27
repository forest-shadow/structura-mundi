---
aliases: []
note_type: article
area: computer-science
domain: networking
section: network-performance
parent: "[[Network Performance]]"
status: seed
related:
  - "[[Network Performance]]"
  - "[[Network Latency]]"
  - "[[Network Packet Loss]]"
tags: []
---

# Network Jitter

## Краткое определение

`Network Jitter` — это статья о вариативности сетевой задержки между последовательными пакетами или событиями передачи.

## Границы темы

- Входит: jitter как variation in latency.
- Не входит: полный разбор всех voice/video buffering strategies.

## Связи с другими заметками

Родительская тема:

`[[Network Performance]]`

Связанные заметки:

- `[[Network Latency]]`
- `[[Network Packet Loss]]`

## Примеры, случаи или следствия

- Даже при приемлемой средней latency высокая вариативность задержки может портить качество real-time communication.
- Jitter особенно заметен в приложениях, чувствительных к неравномерности доставки.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли раздел про buffering и smoothing
- [ ] Проверить `related`
