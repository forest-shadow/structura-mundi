---
aliases:
  - Наблюдаемость
note_type: overview
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Service Reliability]]"
status: seed
related:
  - "[[Telemetry]]"
  - "[[Monitoring]]"
  - "[[Metrics]]"
  - "[[Logging]]"
  - "[[Distributed Tracing]]"
tags:
  - observability
  - reliability
---

# Observability

## Краткое определение области

`Observability` — это обзорная заметка для ветки про наблюдаемость как свойство и инженерную практику вывода внутреннего состояния распределенной системы по ее внешним проявлениям.

## Что входит в эту тему

- `[[Monitoring]]`

## Как устроена ветка

- `Observability` не совпадает с `Telemetry`: телеметрия дает сигналы, а observability задает рамку их интерпретации.
- `Observability` не совпадает с `Monitoring`: monitoring отвечает на заранее известные operational-вопросы и поэтому оформляется как дочерний sub-overview.
- Сигнальные заметки вроде `[[Metrics]]`, `[[Logging]]` и `[[Distributed Tracing]]` остаются соседними в ветке `[[Telemetry]]`, а не переносятся внутрь observability-иерархии.

## Рекомендуемый маршрут чтения

1. Начать с `[[Observability]]` как с общей рамки.
2. Затем сопоставить ее с `[[Telemetry]]`, чтобы не смешивать свойство системы и типы сигналов.
3. После этого перейти к `[[Monitoring]]`.
4. Затем читать `[[Dashboard]]`, `[[Synthetic Monitoring]]` и `[[White-box and Black-box Monitoring]]`.

## Соседние overview-ветки

- `[[Telemetry]]`
- Operational-соседняя ветка пока не добавлена в рабочую структуру.

## Что стоит раскрыть дальше

- [ ] Проверить границы темы
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
