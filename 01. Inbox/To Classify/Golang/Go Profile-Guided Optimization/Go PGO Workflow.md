---
aliases:
  - Go PGO build workflow
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Profile-Guided Optimization]]"
status: seed
related:
  - "[[Go Profile-Guided Optimization]]"
  - "[[Profile-Guided Optimization Feedback Loop]]"
  - "[[Go pprof for PGO]]"
tags: []
---

# Go PGO Workflow

## Краткое определение

`Go PGO Workflow` - это статья о Go-specific процессе применения PGO: от получения profile data до сборки и проверки результата.

## Границы заметки

- Входит: Go-specific build workflow.
- Не входит: общий feedback loop PGO; он относится к `[[Profile-Guided Optimization Feedback Loop]]`.

## Родительская тема

`[[Go Profile-Guided Optimization]]`

## Соседние заметки

- `[[Profile-Guided Optimization Feedback Loop]]`
- `[[Go pprof for PGO]]`

## Что стоит раскрыть дальше

- [ ] Добавить collect -> build -> validate для Go
- [ ] Проверить `related`
