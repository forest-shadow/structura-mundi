---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Distributed Systems]]"
status: seed
related:
  - "[[Distributed Systems]]"
  - "[[Event-Driven Architecture]]"
  - "[[Brokered Messaging Model]]"
  - "[[Publish-Subscribe]]"
  - "[[Producer-Consumer Model]]"
  - "[[Gossip Model]]"
  - "[[Processing Semantics]]"
tags: []
---

# Messaging and Coordination Models

## Краткое определение области

`Messaging and Coordination Models` - это обзорная заметка о более высокоуровневых distributed interaction patterns, в которых важны не только сетевые роли узлов, но и асинхронность, посредники, fan-out, decoupling и распространение состояния.

## Что входит в эту тему

- `[[Brokered Messaging Model]]`
- `[[Publish-Subscribe]]`
- `[[Producer-Consumer Model]]`
- `[[Gossip Model]]`
- `[[Processing Semantics]]`

## Как устроена ветка

- `Brokered Messaging Model` описывает взаимодействие через посредника, а не напрямую между конечными участниками.
- `Publish-Subscribe` описывает модель публикации факта с fan-out доставкой независимым подписчикам.
- `Producer-Consumer Model` фиксирует разделение производства и потребления работы или сообщений.
- `Gossip Model` описывает постепенное, эпидемическое распространение информации по множеству узлов.
- `Processing Semantics` собирает гарантии доставки и обработки, которые определяют, что именно система обещает на границе всей цепочки взаимодействия.

## Рекомендуемый маршрут чтения

1. Начать с `[[Brokered Messaging Model]]` и `[[Publish-Subscribe]]`.
2. Затем перейти к `[[Producer-Consumer Model]]`, чтобы увидеть queue-oriented coordination.
3. После этого перейти к `[[Processing Semantics]]`, если нужно понять гарантийный слой поверх этих моделей.
4. Затем читать `[[Gossip Model]]` как модель распределенного распространения состояния.

## Соседние overview-ветки

- Родительская рамка: `[[Distributed Systems]]`
- Соседняя архитектурная ветка: `[[Event-Driven Architecture]]`
- Соседняя networking-ветка: `[[Network Interaction Models]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Work Queue Model` и `Message-Driven Interaction`
- [ ] Проверить границу между этой веткой и `Event-Driven Architecture`
- [ ] Проверить, нужен ли позже product-specific article `Kafka Delivery Semantics`
- [ ] Проверить `related`
