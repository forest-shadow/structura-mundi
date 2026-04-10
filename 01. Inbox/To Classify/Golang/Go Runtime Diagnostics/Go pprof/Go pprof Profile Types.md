---
aliases:
  - pprof profile types
  - Go pprof profiles
  - Типы профилей pprof в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go pprof]]"
status: seed
related:
  - "[[Go pprof]]"
  - "[[Go Memory Management]]"
  - "[[Go Concurrency Model]]"
  - "[[Go pprof Collection Methods]]"
  - "[[Go pprof Analysis Workflow]]"
tags: []
---

# Go pprof Profile Types

## Краткое определение

`Go pprof Profile Types` - это статья о типах профилей pprof в Go и о том, какие runtime-вопросы каждый профиль помогает исследовать.

## Границы заметки

- Входит: CPU profile, heap profile, goroutine profile, block profile, mutex profile и их диагностический смысл.
- Не входит: способы включения и сбора профилей; они относятся к `[[Go pprof Collection Methods]]`.
- Не входит: пошаговый анализ profile output; он относится к `[[Go pprof Analysis Workflow]]`.

## Родительская тема

`[[Go pprof]]`

## Соседние заметки

- `[[Go Memory Management]]`
- `[[Go Concurrency Model]]`
- `[[Go pprof Collection Methods]]`
- `[[Go pprof Analysis Workflow]]`

## Что стоит раскрыть дальше

- [ ] Добавить краткую карту CPU, heap, goroutine, block и mutex profiles
- [ ] Уточнить, какие профили относятся к allocation behavior, а какие к concurrency contention
- [ ] Проверить `related`
