---
aliases:
  - EDA
  - Событийно-ориентированная архитектура
note_type: overview
area: computer-science
domain: distributed-systems
section: event-driven-architecture
parent:
status: seed
related:
  - "[[Event Collaboration Patterns]]"
  - "[[Publish-Subscribe]]"
  - "[[Transactional Outbox]]"
tags: []
---

# Event-Driven Architecture

## Краткое определение области

Event-Driven Architecture - это архитектурный стиль распределенных систем, в котором компоненты взаимодействуют через события и асинхронную реакцию на них.

## Что входит в эту тему

- паттерны событийного взаимодействия между сервисами;
- инфраструктурные механизмы доставки и маршрутизации событий;
- базовые приемы обеспечения надежности обработки событий.

## Как устроена ветка

- На первом уровне достаточно одной обзорной заметки.
- Один вложенный `overview` оправдан для `Event Collaboration Patterns`.
- Остальные темы пока лучше держать как обычные `article`.

## Рекомендуемый маршрут чтения

1. Начать с этой заметки.
2. Перейти к `Event Collaboration Patterns`.
3. Затем прочитать `Publish-Subscribe`, `Message Broker`, `Transactional Outbox` и `Idempotent Consumer`.

## Соседние overview-ветки

Позже здесь могут появиться связанные ветки по `Event Sourcing`, `CQRS` или `Saga`, но пока они не обязательны для минимальной структуры.

## Что стоит раскрыть дальше

- [ ] Уточнить границы EDA относительно messaging и stream processing.
- [ ] Проверить дочерние статьи.
- [ ] Проверить `related`.
- [ ] Не допустить лишней вложенности.
