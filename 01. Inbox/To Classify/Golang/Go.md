---
aliases:
  - Golang
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Programming Languages]]"
status: seed
related:
  - "[[Programming Languages]]"
  - "[[Go Toolchain]]"
  - "[[Go Type System]]"
  - "[[Go Memory Management]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Runtime Diagnostics]]"
  - "[[Go pprof]]"
  - "[[Go Servers]]"
  - "[[Go Testing]]"
tags: []
---

# Go

## Краткое определение области

`Go` - это обзорная заметка о языке программирования Go как о самостоятельной ветке внутри `Programming Languages`, где соединяются языковая семантика, toolchain, runtime behavior и production-oriented engineering practices.

## Что входит в эту тему

- `[[Go Toolchain]]`
- `[[Go Packages and Modules]]`
- `[[Go Type System]]`
- `[[Go Error Handling]]`
- `[[Go Memory Management]]`
- `[[Go Concurrency Model]]`
- `[[Go Runtime Diagnostics]]`
- `[[Go Servers]]`
- `[[Go Testing]]`

## Как устроена ветка

- `Go Toolchain` и `Go Packages and Modules` задают инженерную и build-oriented рамку.
- `Go Type System` собирает language semantics и type-related notes.
- `Go Memory Management` и `Go Concurrency Model` удерживают runtime и execution behavior.
- `Go Runtime Diagnostics` собирает инструменты и практики диагностики runtime-поведения, включая `[[Go pprof]]`.
- `Go Servers` выносит в отдельный sub-overview production-oriented тему написания серверов на Go, не смешивая ее ни с общей теорией `[[Server]]`, ни с голой concurrency-model.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Toolchain]]` и `[[Go Packages and Modules]]`.
2. Затем перейти к `[[Go Type System]]`.
3. После этого читать `[[Go Memory Management]]` и `[[Go Concurrency Model]]`.
4. Затем перейти к `[[Go Runtime Diagnostics]]`, если нужен profiling и runtime-analysis контекст.
5. Затем перейти к `[[Go Servers]]`, если нужен server-side инженерный взгляд.
6. Завершить `[[Go Testing]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Programming Languages]]`
- Смежная cross-language ветка: `[[Compilation]]`

## Что стоит раскрыть дальше

- [ ] Проверить границу между `Go Concurrency Model` и `Go Servers`
- [ ] Проверить границу между `Go Runtime Diagnostics`, `Go Memory Management` и `Go Servers`
- [ ] Решить, когда внутри `Go Servers` понадобятся notes про middleware и RPC contracts
- [ ] Проверить `related`
