---
aliases:
  - Паттерны событийного взаимодействия
note_type: overview
area: computer-science
domain: distributed-systems
section: event-driven-architecture
parent: "[[Event-Driven Architecture]]"
status: seed
related:
  - "[[Event Notification]]"
  - "[[Event-Carried State Transfer]]"
  - "[[Competing Consumers]]"
tags: []
---

# Event Collaboration Patterns

## Краткое определение области

Этот обзорный узел собирает паттерны, через которые сервисы координируют работу с помощью событий, а не прямых синхронных вызовов.

## Что входит в эту тему

- `Event Notification`
- `Event-Carried State Transfer`
- `Competing Consumers`

## Как устроена ветка

- Вложенный `overview` здесь оправдан, потому что это отдельный устойчивый кластер внутри EDA.
- Ниже этого уровня лучше оставаться на плоском наборе `article`, если не появится самостоятельный корпус по каждому подтипу.

## Рекомендуемый маршрут чтения

1. Понять общий смысл collaboration patterns.
2. Перейти к `Event Notification`.
3. Затем прочитать `Event-Carried State Transfer` и `Competing Consumers`.

## Соседние overview-ветки

Соседние обзорные ветки пока не создаются.

## Что стоит раскрыть дальше

- [ ] Уточнить различия между collaboration patterns.
- [ ] Проверить связь с messaging infrastructure.
- [ ] Проверить `related`.
- [ ] Не разрастать ветку глубже без необходимости.
