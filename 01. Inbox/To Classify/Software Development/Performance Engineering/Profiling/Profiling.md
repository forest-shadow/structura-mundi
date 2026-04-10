---
aliases:
  - Software Profiling
  - Code Profiling
  - Performance Profiling
note_type: overview
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Performance Engineering]]"
status: seed
related:
  - "[[Performance Engineering]]"
  - "[[Profiling Targets and Signals]]"
  - "[[Profiling Workflow]]"
  - "[[Profiling Overhead and Limits]]"
  - "[[Performance Modeling]]"
  - "[[Go pprof]]"
tags: []
---

# Profiling

## Краткое определение области

`Profiling` - это инженерная практика измерения того, где и на что программа реально тратит время, память и другие ресурсы во время исполнения.

## Что входит в эту тему

- `[[Profiling Targets and Signals]]`
- `[[Profiling Workflow]]`
- `[[Profiling Overhead and Limits]]`

## Как устроена ветка

- `Profiling Targets and Signals` удерживает вопрос "что именно измеряется" и какие типы профилей дают разные ответы.
- `Profiling Workflow` удерживает путь от гипотезы и сбора профиля к интерпретации и следующему циклу оптимизации.
- `Profiling Overhead and Limits` удерживает ограничения метода: смещение результатов, sampling bias, instrumentation cost и неверные выводы.

## Рекомендуемый маршрут чтения

1. Начать с `[[Profiling Targets and Signals]]`.
2. Затем перейти к `[[Profiling Workflow]]`.
3. После этого читать `[[Profiling Overhead and Limits]]`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `CPU Profiling`, `Memory Profiling` и `Concurrency Profiling` как отдельные notes
- [ ] Проверить границу между profiling, benchmarking и tracing
- [ ] Проверить `related`
