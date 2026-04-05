---
aliases:
  - Exactly Once Semantics
  - Exactly-once Processing
  - Exactly-once Delivery
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Processing Semantics]]"
status: seed
related:
  - "[[Processing Semantics]]"
  - "[[At-Least-Once Delivery]]"
  - "[[Effectively-Once Processing]]"
  - "[[Kafka]]"
tags: []
---

# Exactly-Once Semantics

## Краткое определение

`Exactly-Once Semantics` — это перегруженный термин для гарантий, при которых система заявляет однократный результат обработки в пределах явно заданной границы, но сама эта граница должна быть отдельно уточнена.

## Основная идея или механизм

Нужно раскрыть, что exactly-once почти никогда не означает магическую глобальную гарантию для всей распределенной бизнес-цепочки; обычно речь идет о более узком контуре хранения, чтения, commit coordination или stream-processing runtime.

## Границы темы

- Входит: формальная граница гарантии, coordination cost, stateful processing, transaction boundary.
- Не входит: неявное обещание, что любой внешний побочный эффект в системе тоже произойдет ровно один раз.

## Связи с другими заметками

Родительская тема:

`[[Processing Semantics]]`

Связанные заметки:

- `[[At-Least-Once Delivery]]`
- `[[Effectively-Once Processing]]`
- `[[Kafka]]`

## Примеры, случаи или следствия

Добавить 1-3 примера, где infrastructure-level exactly-once не равен global business exactly-once.

## Что стоит раскрыть дальше

- [ ] Уточнить, в какой именно границе понимается guarantee
- [ ] Добавить сравнение с `Effectively-Once Processing`
- [ ] Проверить `aliases`
- [ ] Проверить `related`
