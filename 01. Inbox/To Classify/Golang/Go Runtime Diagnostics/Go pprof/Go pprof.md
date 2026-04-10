---
aliases:
  - pprof
  - go tool pprof
  - runtime/pprof
  - net/http/pprof
  - Go profiling with pprof
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Runtime Diagnostics]]"
status: seed
related:
  - "[[Go Runtime Diagnostics]]"
  - "[[Go Toolchain]]"
  - "[[Go Memory Management]]"
  - "[[Go Concurrency Model]]"
  - "[[Profiling]]"
  - "[[Observability in Go Servers]]"
  - "[[Go pprof Profile Types]]"
  - "[[Go pprof Collection Methods]]"
  - "[[Go pprof Analysis Workflow]]"
tags: []
---

# Go pprof

## Краткое определение области

`Go pprof` - это обзорный узел о pprof в контексте Go: сборе, экспорте и анализе runtime-профилей Go-программ через стандартные пакеты и инструменты Go.

## Что входит в эту тему

- `[[Go pprof Profile Types]]`
- `[[Go pprof Collection Methods]]`
- `[[Go pprof Analysis Workflow]]`

## Как устроена ветка

- `Profiling` остается более общей cross-language практикой, а `Go pprof` описывает ее реализацию через стандартные пакеты и утилиты Go.
- `Go pprof Profile Types` удерживает типы профилей и смысл сигналов.
- `Go pprof Collection Methods` удерживает способы получения профилей из тестов, приложений и HTTP/debug endpoints.
- `Go pprof Analysis Workflow` удерживает практику чтения профилей и перехода от profile data к гипотезам об узких местах.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go pprof Profile Types]]`.
2. Затем перейти к `[[Go pprof Collection Methods]]`.
3. После этого читать `[[Go pprof Analysis Workflow]]`.
4. Для memory-related выводов сопоставлять с `[[Go Memory Management]]`, а для серверного operational-контекста - с `[[Observability in Go Servers]]`.

## Соседние overview-ветки

- `[[Go Runtime Diagnostics]]`
- `[[Go Toolchain]]`
- `[[Go Memory Management]]`
- `[[Observability in Go Servers]]`

## Что стоит раскрыть дальше

- [ ] Проверить границу между pprof и execution tracing
- [ ] Решить, когда нужны отдельные заметки для CPU, heap и goroutine profiles
- [ ] Проверить `aliases`
- [ ] Проверить `related`
