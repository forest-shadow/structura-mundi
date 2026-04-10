---
aliases:
  - PGO Constraints and Trade-offs
  - PGO Limits and Trade-offs
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Profile-Guided Optimization]]"
status: seed
related:
  - "[[Profile-Guided Optimization]]"
  - "[[Profile-Guided Optimization Profile Collection]]"
  - "[[Profile-Guided Optimization Feedback Loop]]"
  - "[[Go PGO Constraints and Trade-offs]]"
tags: []
---

# Profile-Guided Optimization Constraints and Trade-offs

## Краткое определение

`Profile-Guided Optimization Constraints and Trade-offs` - это статья об ограничениях, рисках и инженерных компромиссах PGO как общего compilation-подхода.

## Границы заметки

- Входит: нерепрезентативные профили, стоимость сбора профиля, переносимость результатов и риск локальной оптимизации под неправильную нагрузку.
- Не входит: сам цикл применения профиля; он относится к `[[Profile-Guided Optimization Feedback Loop]]`.
- Не входит: Go-specific implementation details; они относятся к `[[Go PGO Constraints and Trade-offs]]`.

## Родительская тема

`[[Profile-Guided Optimization]]`

## Соседние заметки

- `[[Profile-Guided Optimization Profile Collection]]`
- `[[Profile-Guided Optimization Feedback Loop]]`
- `[[Go PGO Constraints and Trade-offs]]`

## Что стоит раскрыть дальше

- [ ] Добавить риск профиля, снятого с нерепрезентативной нагрузки
- [ ] Уточнить стоимость обновления профилей в build pipeline
- [ ] Проверить `related`
