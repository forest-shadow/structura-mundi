---
aliases:
  - Go PGO
  - PGO in Go
  - Profile-Guided Optimization in Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Toolchain]]"
status: seed
related:
  - "[[Go Toolchain]]"
  - "[[Profile-Guided Optimization]]"
  - "[[Go pprof]]"
  - "[[Go pprof for PGO]]"
  - "[[Go PGO Workflow]]"
  - "[[Go PGO Constraints and Trade-offs]]"
tags: []
---

# Go Profile-Guided Optimization

## Краткое определение области

`Go Profile-Guided Optimization` - это обзорная ветка о language-specific реализации PGO в экосистеме Go.

## Что входит в эту тему

- `[[Go pprof for PGO]]`
- `[[Go PGO Workflow]]`
- `[[Go PGO Constraints and Trade-offs]]`

## Как устроена ветка

- `Go Profile-Guided Optimization` живёт под `[[Go Toolchain]]`, потому что речь идёт о compiler- и build-workflow.
- `Profile-Guided Optimization` остаётся общим cross-language concept, а эта ветка выражает Go-specific случай.
- `Go pprof for PGO` удерживает роль pprof как источника профильных данных для Go PGO.

## Рекомендуемый маршрут чтения

1. Начать с `[[Profile-Guided Optimization]]` как общей рамки.
2. Затем перейти к `[[Go pprof for PGO]]`.
3. После этого читать `[[Go PGO Workflow]]` и `[[Go PGO Constraints and Trade-offs]]`.

## Соседние overview-ветки

- `[[Go Toolchain]]`
- `[[Profile-Guided Optimization]]`
- `[[Go Runtime Diagnostics]]`

## Что стоит раскрыть дальше

- [ ] Уточнить связь между общим PGO concept и Go-specific workflow
- [ ] Проверить `related`
