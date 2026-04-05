---
aliases:
  - End-to-End Processing Semantics
  - Delivery and Processing Semantics
  - Системная семантика доставки и обработки
  - Сквозная семантика обработки
note_type: overview
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Messaging and Coordination Models]]"
status: seed
related:
  - "[[Messaging and Coordination Models]]"
  - "[[Event-Driven Architecture]]"
  - "[[Kafka]]"
  - "[[Transactional Outbox]]"
  - "[[Idempotent Consumer]]"
  - "[[Dual Write]]"
tags: []
---

# Processing Semantics

## Краткое определение области

`Processing Semantics` — это обзорная заметка о том, какие гарантии система реально дает на границе полной цепочки обработки: от публикации и доставки сообщения до повторной обработки, фиксации результата и наблюдаемого бизнес-эффекта.

## Что входит в эту тему

- `[[At-Most-Once Delivery]]`
- `[[At-Least-Once Delivery]]`
- `[[Exactly-Once Semantics]]`
- `[[Effectively-Once Processing]]`

## Как устроена ветка

- `At-Most-Once Delivery` и `At-Least-Once Delivery` задают базовые модели гарантий доставки.
- `Exactly-Once Semantics` разбирает перегруженный термин, который часто обещает больше, чем реально гарантирует end-to-end цепочка.
- `Effectively-Once Processing` описывает практическую цель прикладной системы: получить корректный итоговый эффект несмотря на повторы, ретраи и частичные сбои.
- Product-specific темы вроде `Kafka Delivery Semantics` лучше позже связывать с этой веткой через `related`, а не подменять ими абстрактный обзорный узел.

## Рекомендуемый маршрут чтения

1. Начать с этой заметки.
2. Затем прочитать `[[At-Most-Once Delivery]]` и `[[At-Least-Once Delivery]]`.
3. После этого перейти к `[[Exactly-Once Semantics]]`.
4. Затем прочитать `[[Effectively-Once Processing]]`.
5. После этого перейти к `[[Transactional Outbox]]`, `[[Idempotent Consumer]]` и `[[Kafka]]` как к прикладным механизмам и контекстам.

## Соседние overview-ветки

- Родительская рамка: `[[Messaging and Coordination Models]]`
- Соседняя архитектурная ветка: `[[Event-Driven Architecture]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границу между `delivery` и `processing`
- [ ] Проверить, нужен ли позже отдельный article `Kafka Delivery Semantics`
- [ ] Добавить больше связей с `Dual Write` и `Transactional Outbox`
- [ ] Проверить `aliases`
- [ ] Проверить `related`
