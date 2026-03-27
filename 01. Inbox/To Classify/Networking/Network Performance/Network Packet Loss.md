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
  - "[[Network Throughput]]"
  - "[[Network Latency]]"
  - "[[Network Jitter]]"
tags: []
---

# Network Packet Loss

## Краткое определение

`Network Packet Loss` — это статья о ситуации, в которой часть пакетов не достигает получателя и не участвует в успешной доставке данных.

## Границы темы

- Входит: packet loss как базовая network-quality metric.
- Не входит: полный разбор всех протокольных механизмов восстановления потерь.

## Связи с другими заметками

Родительская тема:

`[[Network Performance]]`

Связанные заметки:

- `[[Network Throughput]]`
- `[[Network Latency]]`
- `[[Network Jitter]]`

## Примеры, случаи или следствия

- Packet loss может уменьшать throughput и усиливать воспринимаемую нестабильность соединения.
- Даже небольшой loss может заметно влиять на некоторые протоколы и real-time workloads.

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужен раздел про retransmission and recovery
- [ ] Проверить `related`
