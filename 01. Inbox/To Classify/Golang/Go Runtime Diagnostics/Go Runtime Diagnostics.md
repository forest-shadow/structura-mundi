---
aliases:
  - Runtime Diagnostics in Go
  - Go Diagnostics
  - Диагностика runtime в Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Toolchain]]"
  - "[[Go Memory Management]]"
  - "[[Go Concurrency Model]]"
  - "[[Go pprof]]"
  - "[[Observability in Go Servers]]"
tags: []
---

# Go Runtime Diagnostics

## Краткое определение области

`Go Runtime Diagnostics` - это обзорная ветка про инструменты и практики диагностики поведения Go-программ во время выполнения: профилирование, анализ runtime-сигналов, поиск bottleneck-ов и интерпретацию стоимости CPU, памяти, блокировок и горутин.

## Что входит в эту тему

- `[[Go pprof]]`

## Как устроена ветка

- `Go Runtime Diagnostics` живёт внутри `[[Go]]`, потому что речь идет о language-specific runtime behavior и стандартном toolchain Go.
- `Go pprof` является первым дочерним overview-узлом, потому что pprof объединяет несколько типов профилей и несколько способов сбора данных.
- Связь с `[[Observability in Go Servers]]` поперечная: серверная observability использует pprof как один из диагностических сигналов, но pprof не сводится только к серверному сценарию.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go pprof]]`.
2. Затем перейти к типам профилей, способам сбора и workflow анализа.
3. Для memory-related интерпретации сопоставлять с `[[Go Memory Management]]`.
4. Для server-side production-контекста сопоставлять с `[[Observability in Go Servers]]`.

## Соседние overview-ветки

- `[[Go Toolchain]]`
- `[[Go Memory Management]]`
- `[[Go Concurrency Model]]`
- `[[Go Servers]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Go Execution Tracer`, `Go Runtime Metrics` и `Go Debugging`
- [ ] Проверить границу между runtime diagnostics и server observability
- [ ] Проверить `related`
