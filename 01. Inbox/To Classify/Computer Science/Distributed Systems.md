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
- `[[Event-Driven Architecture]]`
- `[[Dual Write]]`
- `[[Telemetry]]`

## Как устроена ветка

- `Distributed Systems Problems` собирает фундаментальные ограничения и классы проблем;
- `Event-Driven Architecture` и `Dual Write` представляют более прикладные архитектурные кластеры;
- `Telemetry` стоит рядом как operationally важная ветка внутри распределенных систем.

## Рекомендуемый маршрут чтения

1. Начать с `[[Distributed Systems Problems]]`.
2. Затем перейти к `[[Event-Driven Architecture]]` и `[[Dual Write]]`.
3. После этого читать `[[Telemetry]]` как operational branch.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Проверить, что domain-root overview остается без `section`
- [ ] Решить, нужен ли позже отдельный узел для consistency models
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
