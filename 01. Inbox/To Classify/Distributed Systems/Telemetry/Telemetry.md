---
aliases:
  - Телеметрия
  - Telemetry and Metrics
note_type: overview
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Service Reliability]]"
status: seed
related:
  - "[[Metrics]]"
  - "[[Logging]]"
  - "[[Distributed Tracing]]"
  - "[[Observability]]"
tags:
  - observability
  - reliability
---

# Telemetry

## Краткое определение области

Обзорная заметка для телеметрии как общего класса наблюдаемых сигналов и данных, собираемых о поведении системы.

## Что входит в эту тему

- `[[Metrics]]`
- `[[Logging]]`
- `[[Distributed Tracing]]`

## Как устроена ветка

- `Telemetry` выступает родовым понятием.
- `Metrics` является отдельной подветкой как специализированный числовой класс телеметрии.
- `Logging` и `Distributed Tracing` остаются соседними видами телеметрических сигналов.

## Рекомендуемый маршрут чтения

1. Начать с `[[Telemetry]]` как общей рамки.
2. Затем перейти к `[[Metrics]]`.
3. После этого сравнить ее с `[[Logging]]` и `[[Distributed Tracing]]`.

## Соседние overview-ветки

- `[[Observability]]`

## Что стоит раскрыть дальше

- [ ] Проверить границы темы
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
