---
aliases:
  - Apache Kafka
note_type: overview
area: computer-science
domain: distributed-systems
section: kafka
parent: "[[Distributed Systems]]"
status: seed
related:
  - "[[Messaging and Coordination Models]]"
  - "[[Brokered Messaging Model]]"
  - "[[Message Broker]]"
  - "[[Publish-Subscribe]]"
  - "[[Producer-Consumer Model]]"
  - "[[Event-Driven Architecture]]"
  - "[[Transactional Outbox]]"
tags: []
---

# Kafka

## Краткое определение области

`Kafka` — это section-level overview внутри `distributed-systems` для заметок о Kafka как распределенной платформе журналирования и доставки событийных потоков: ее модели хранения, логике чтения, координации потребителей и типичных архитектурных сценариях использования.

## Что входит в эту тему

- `[[Kafka Topic]]`
- `[[Kafka Partition]]`
- `[[Kafka Consumer Group]]`
- `[[Kafka Offset]]`
- `[[Kafka Delivery Semantics]]`

## Как устроена ветка

- `Kafka` оправдан как отдельный overview-узел, потому что рядом с ним естественно собираются product-specific темы про topics, partitions, offsets, consumer groups, retention и delivery guarantees.
- `Kafka Delivery Semantics` уже оправдан как вложенный overview, потому что внутри него есть устойчивый набор соседних статей про at-most-once, at-least-once и exactly-once behavior.
- На текущем этапе все еще не нужно вводить дополнительный уровень вроде `Kafka Internals`, пока внутри ветки нет устойчивого корпуса соседних заметок про replication, controllers и rebalancing.
- Поперечная связь с `[[Brokered Messaging Model]]`, `[[Publish-Subscribe]]` и `[[Producer-Consumer Model]]` важна, но она не заменяет product-specific оптику: Kafka здесь рассматривается как конкретная технология, а не просто как абстрактный messaging pattern.

## Рекомендуемый маршрут чтения

1. Начать с `[[Kafka Topic]]` как основной логической единицы организации потока.
2. Затем перейти к `[[Kafka Partition]]`, чтобы понять масштабирование и порядок сообщений.
3. После этого читать `[[Kafka Consumer Group]]` и `[[Kafka Offset]]`, чтобы собрать модель чтения и координации потребителей.
4. Затем перейти к `[[Kafka Delivery Semantics]]`, чтобы увидеть, как эта модель влияет на потери, дублирование и transactional coordination.

## Соседние overview-ветки

- Родительская рамка: `[[Distributed Systems]]`
- Соседняя абстрактная ветка: `[[Messaging and Coordination Models]]`
- Соседняя архитектурная ветка: `[[Event-Driven Architecture]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про retention, log compaction и rebalancing
- [ ] Решить, когда нужен отдельный overview про Kafka internals
- [ ] Проверить границы `Kafka Delivery Semantics`
- [ ] Проверить `related`
