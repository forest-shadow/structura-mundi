---
aliases:
  - PGO Profile Collection
  - Profile collection for PGO
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Profile-Guided Optimization]]"
status: seed
related:
  - "[[Profile-Guided Optimization]]"
  - "[[Profile-Guided Optimization Feedback Loop]]"
  - "[[Go pprof for PGO]]"
tags: []
---

# Profile-Guided Optimization Profile Collection

## Краткое определение

`Profile-Guided Optimization Profile Collection` - это статья о том, как для PGO получают профильные данные и почему качество workload-а определяет качество последующей оптимизации.

## Границы заметки

- Входит: representative workloads, profile quality, sampling vs instrumentation и происхождение profile data.
- Не входит: сам optimization loop компилятора; он относится к `[[Profile-Guided Optimization Feedback Loop]]`.
- Не входит: language-specific mechanics вроде `[[Go pprof for PGO]]` как отдельного случая.

## Родительская тема

`[[Profile-Guided Optimization]]`

## Соседние заметки

- `[[Profile-Guided Optimization Feedback Loop]]`
- `[[Profile-Guided Optimization Constraints and Trade-offs]]`
- `[[Go pprof for PGO]]`

## Что стоит раскрыть дальше

- [ ] Добавить различие между sampling-based и instrumentation-based profile collection
- [ ] Уточнить требования к representative workload
- [ ] Проверить `related`
