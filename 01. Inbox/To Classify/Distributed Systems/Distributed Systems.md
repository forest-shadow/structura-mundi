---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Distributed Systems Problems]]"
  - "[[Caching]]"
  - "[[Event-Driven Architecture]]"
  - "[[Dual Write]]"
  - "[[Telemetry]]"
tags: []
---

# Distributed Systems

## Краткое определение области

`Distributed Systems` — это доменная обзорная заметка для веток про системы, где вычисление и данные распределены по нескольким узлам, а ключевые проблемы возникают из-за отказов, времени, репликации и координации.

## Что входит в эту тему

- `[[Distributed Systems Problems]]`
- `[[Caching]]`
- `[[Event-Driven Architecture]]`
- `[[Telemetry]]`

## Как устроена ветка

- `Distributed Systems Problems` собирает фундаментальные ограничения и классы проблем, включая уже оформившуюся дочернюю ветку `[[Dual Write]]`;
- `Caching` собирает performance-oriented branch про снижение latency, уменьшение нагрузки и trade-offs консистентности;
- `Event-Driven Architecture` уже выступает как самостоятельная архитектурная подветка, а не как одиночная заметка;
- `Telemetry` стоит рядом как operationally важная ветка внутри распределенных систем.

## Рекомендуемый маршрут чтения

1. Начать с `[[Distributed Systems Problems]]`.
2. Внутри этой рамки отдельно перейти к `[[Dual Write]]` как к практическому problem-cluster.
3. Затем перейти к `[[Caching]]` как к performance branch поверх базовых distributed-systems constraints.
4. После этого перейти к `[[Event-Driven Architecture]]`.
5. Затем читать `[[Telemetry]]` как operational branch.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Проверить, что domain-root overview остается без `section`
- [ ] Решить, нужен ли позже отдельный узел для consistency models
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
