---
aliases:
  - pprof analysis workflow
  - Analyzing pprof profiles in Go
  - Анализ профилей pprof в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go pprof]]"
status: seed
related:
  - "[[Go pprof]]"
  - "[[Go Toolchain]]"
  - "[[Go Memory Management]]"
  - "[[Go pprof Profile Types]]"
  - "[[Go pprof Collection Methods]]"
tags: []
---

# Go pprof Analysis Workflow

## Краткое определение

`Go pprof Analysis Workflow` - это статья о том, как читать pprof-профили Go-программ и превращать profile data в диагностические гипотезы.

## Границы заметки

- Входит: `go tool pprof`, top/list/web-представления, поиск hot paths, сравнение профилей и связь результата с изменениями кода.
- Не входит: выбор типа профиля; он относится к `[[Go pprof Profile Types]]`.
- Не входит: механика получения профиля; она относится к `[[Go pprof Collection Methods]]`.

## Родительская тема

`[[Go pprof]]`

## Соседние заметки

- `[[Go Toolchain]]`
- `[[Go Memory Management]]`
- `[[Go pprof Profile Types]]`
- `[[Go pprof Collection Methods]]`

## Что стоит раскрыть дальше

- [ ] Добавить базовый маршрут анализа CPU profile
- [ ] Добавить базовый маршрут анализа heap profile
- [ ] Добавить типичные ошибки интерпретации pprof output
- [ ] Проверить `related`
