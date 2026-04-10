---
aliases:
  - Software Performance Engineering
note_type: overview
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Software Development]]"
status: seed
related:
  - "[[Software Development]]"
  - "[[Profiling]]"
  - "[[Performance Modeling]]"
  - "[[Go Runtime Diagnostics]]"
  - "[[Go pprof]]"
tags: []
---

# Performance Engineering

## Краткое определение области

`Performance Engineering` - это обзорная ветка про инженерные практики измерения, интерпретации и улучшения реального поведения программ во время исполнения.

## Что входит в эту тему

- `[[Profiling]]`

## Как устроена ветка

- `Performance Engineering` живет внутри `[[Software Development]]`, потому что речь идет о workflow и инструментах разработчика, а не о формальной теории системной нагрузки.
- `[[Performance Modeling]]` остается соседней математической веткой: она объясняет очереди, throughput и saturation, но не подменяет практику чтения профилей.
- language-specific инструменты вроде `[[Go pprof]]` и `[[Go Runtime Diagnostics]]` связаны с этой веткой поперечно как частные случаи.

## Рекомендуемый маршрут чтения

1. Начать с `[[Profiling]]`.
2. Затем перейти к `[[Profiling Targets and Signals]]`.
3. После этого читать `[[Profiling Workflow]]` и `[[Profiling Overhead and Limits]]`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Benchmarking` и `Performance Regression Analysis`
- [ ] Проверить границу между performance engineering и observability
- [ ] Проверить `related`
