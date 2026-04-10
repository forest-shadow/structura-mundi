---
aliases:
  - Мониторинг
note_type: overview
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Observability]]"
status: seed
related:
  - "[[Observability]]"
  - "[[Telemetry]]"
  - "[[Dashboard]]"
  - "[[Synthetic Monitoring]]"
  - "[[White-box and Black-box Monitoring]]"
tags:
  - observability
  - reliability
---

# Monitoring

## Краткое определение области

`Monitoring` — это обзорная заметка для monitoring-практик, в которых система регулярно наблюдается по заранее выбранным сигналам, порогам и operational-сценариям.

## Что входит в эту тему

- `[[Dashboard]]`
- `[[Synthetic Monitoring]]`
- `[[White-box and Black-box Monitoring]]`

## Как устроена ветка

- `Monitoring` является дочерней overview-веткой внутри `[[Observability]]`, потому что monitoring уже, чем observability, и работает в пространстве заранее известных вопросов.
- `Dashboard` собирает слой визуализации и навигации по сигналам.
- `Synthetic Monitoring` описывает активные проверки извне, а не пассивное чтение внутренних сигналов.
- `White-box and Black-box Monitoring` фиксирует базовое различие между внутренним и внешним наблюдением системы.

## Рекомендуемый маршрут чтения

1. Начать с `[[Monitoring]]`.
2. Затем перейти к `[[White-box and Black-box Monitoring]]`, чтобы зафиксировать базовые режимы наблюдения.
3. После этого читать `[[Synthetic Monitoring]]`.
4. Затем перейти к `[[Dashboard]]` как к практическому слою визуализации сигналов.

## Соседние overview-ветки

- Родительская рамка: `[[Observability]]`
- Сигнальная соседняя ветка: `[[Telemetry]]`
- Operational-соседняя ветка пока не добавлена в рабочую структуру.

## Что стоит раскрыть дальше

- [ ] Проверить границы темы
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
