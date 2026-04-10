---
aliases:
  - pprof collection methods
  - Collecting pprof profiles in Go
  - Способы сбора pprof в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go pprof]]"
status: seed
related:
  - "[[Go pprof]]"
  - "[[Go Toolchain]]"
  - "[[Observability in Go Servers]]"
  - "[[Go pprof Profile Types]]"
  - "[[Go pprof Analysis Workflow]]"
tags: []
---

# Go pprof Collection Methods

## Краткое определение

`Go pprof Collection Methods` - это статья о способах получить pprof-профили в Go-программах, тестах и production-like окружениях.

## Границы заметки

- Входит: `runtime/pprof`, `net/http/pprof`, benchmark flags, CPU/heap profile files и controlled debug endpoints.
- Не входит: детальная интерпретация профилей; она относится к `[[Go pprof Analysis Workflow]]`.
- Не входит: общая observability-архитектура сервера; она относится к `[[Observability in Go Servers]]`.

## Родительская тема

`[[Go pprof]]`

## Соседние заметки

- `[[Go Toolchain]]`
- `[[Observability in Go Servers]]`
- `[[Go pprof Profile Types]]`
- `[[Go pprof Analysis Workflow]]`

## Что стоит раскрыть дальше

- [ ] Добавить различие между programmatic collection и HTTP/debug endpoints
- [ ] Добавить правило не выставлять pprof endpoints на публичный listener
- [ ] Уточнить связь с benchmark-driven profiling
- [ ] Проверить `related`
