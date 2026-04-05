---
aliases:
  - At Least Once Delivery
  - At-least-once
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Processing Semantics]]"
status: seed
related:
  - "[[Processing Semantics]]"
  - "[[At-Most-Once Delivery]]"
  - "[[Exactly-Once Semantics]]"
  - "[[Effectively-Once Processing]]"
  - "[[Idempotent Consumer]]"
tags: []
---

# At-Least-Once Delivery

## Краткое определение

`At-Least-Once Delivery` — это семантика, при которой система стремится не потерять сообщение и поэтому допускает его повторную доставку и повторную обработку.

## Основная идея или механизм

Нужно раскрыть, как подтверждения, ретраи и неопределенность на границе `ack/commit` делают дубликаты расчетной частью модели, а не исключением.

## Границы темы

- Входит: повторная доставка, retries, возможные дубликаты, необходимость идемпотентности или дедупликации.
- Не входит: автоматическая гарантия единственного наблюдаемого бизнес-результата.

## Связи с другими заметками

Родительская тема:

`[[Processing Semantics]]`

Связанные заметки:

- `[[At-Most-Once Delivery]]`
- `[[Exactly-Once Semantics]]`
- `[[Effectively-Once Processing]]`
- `[[Idempotent Consumer]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария с повторной публикацией, replay или consumer retry.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить примеры `ack/commit` boundary
- [ ] Проверить `aliases`
- [ ] Проверить `related`
