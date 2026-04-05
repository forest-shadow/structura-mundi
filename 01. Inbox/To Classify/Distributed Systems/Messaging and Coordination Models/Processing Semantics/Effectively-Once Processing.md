---
aliases:
  - Effective-Once Processing
  - End-to-End Exactly-Once
  - Эффективно однократная обработка
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Processing Semantics]]"
status: seed
related:
  - "[[Processing Semantics]]"
  - "[[At-Least-Once Delivery]]"
  - "[[Exactly-Once Semantics]]"
  - "[[Transactional Outbox]]"
  - "[[Idempotent Consumer]]"
  - "[[Dual Write]]"
tags: []
---

# Effectively-Once Processing

## Краткое определение

`Effectively-Once Processing` — это практическая end-to-end семантика, при которой система допускает повторы на уровне доставки, но организует обработку так, чтобы итоговый наблюдаемый бизнес-результат был эквивалентен однократному выполнению.

## Основная идея или механизм

Нужно раскрыть, что эта гарантия достигается не одним транспортным свойством, а комбинацией механизмов: идемпотентности, дедупликации, координации commit points, transactional outbox и явного контроля границы побочных эффектов.

## Границы темы

- Входит: end-to-end boundary, business outcome, idempotency, deduplication, side-effect control.
- Не входит: упрощенное отождествление с transport-level exactly-once.

## Связи с другими заметками

Родительская тема:

`[[Processing Semantics]]`

Связанные заметки:

- `[[At-Least-Once Delivery]]`
- `[[Exactly-Once Semantics]]`
- `[[Transactional Outbox]]`
- `[[Idempotent Consumer]]`
- `[[Dual Write]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария, где at-least-once delivery вместе с идемпотентной обработкой дает effectively-once outcome.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить явную границу between delivery and business effect
- [ ] Проверить `aliases`
- [ ] Проверить `related`
