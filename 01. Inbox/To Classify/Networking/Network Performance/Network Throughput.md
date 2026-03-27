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
  - "[[Network Bandwidth]]"
  - "[[Network Packet Loss]]"
  - "[[Network Latency]]"
tags: []
---

# Network Throughput

## Краткое определение

`Network Throughput` — это статья о фактической скорости успешной передачи данных через сеть.

## Границы темы

- Входит: throughput как achieved transfer rate.
- Не входит: полный разбор benchmark methodology и всех application-specific metrics.

## Связи с другими заметками

Родительская тема:

`[[Network Performance]]`

Связанные заметки:

- `[[Network Bandwidth]]`
- `[[Network Packet Loss]]`
- `[[Network Latency]]`

## Примеры, случаи или следствия

- Throughput обычно ниже bandwidth из-за protocol overhead, congestion, retransmissions и других ограничений.
- Сравнение throughput без учета latency и packet loss часто дает слишком грубую картину поведения сети.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли отдельный раздел про goodput
- [ ] Проверить `related`
