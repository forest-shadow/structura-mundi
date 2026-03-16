---
aliases:
  - Перцентиль
note_type: article
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Metrics]]"
status: seed
related:
  - "[[Metrics]]"
  - "[[Histogram]]"
tags:
  - observability
  - performance
---

# Percentile

## Краткое определение

Каноническая статья для percentiles как способа описания хвостов распределения в метрических системах.

## Основная идея или механизм

Нужно объяснить, почему p95/p99 дают более полезную operational picture, чем average, особенно в распределенных сервисах.

## Границы темы

- Что относится к квантильному описанию распределения.
- Где тема переходит в histogram approximation и SLI/SLO practice.

## Связи с другими заметками

Родительская тема:

`[[Metrics]]`

Связанные заметки:

- `[[Histogram]]`

## Примеры, случаи или следствия

Добавить пример различия между average latency и p99 latency.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
