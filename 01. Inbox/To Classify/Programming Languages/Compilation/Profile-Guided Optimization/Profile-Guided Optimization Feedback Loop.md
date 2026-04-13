---
aliases:
  - PGO Feedback Loop
  - PGO Optimization Loop
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Profile-Guided Optimization]]"
status: seed
related:
  - "[[Profile-Guided Optimization]]"
  - "[[Profile-Guided Optimization Profile Collection]]"
  - "[[Go PGO Workflow]]"
tags: []
---

# Profile-Guided Optimization Feedback Loop

## Краткое определение

`Profile-Guided Optimization Feedback Loop` - это статья о цикле PGO: сбор профиля, повторная сборка с profile data и проверка эффекта оптимизации.

## Границы заметки

- Входит: feedback loop между execution profile и compiler optimization decisions.
- Не входит: общие ограничения и риски PGO; они относятся к `[[Profile-Guided Optimization Constraints and Trade-offs]]`.
- Не входит: языкоспецифичный workflow вроде `[[Go PGO Workflow]]`.

## Родительская тема

`[[Profile-Guided Optimization]]`

## Соседние заметки

- `[[Profile-Guided Optimization Profile Collection]]`
- `[[Profile-Guided Optimization Constraints and Trade-offs]]`
- `[[Go PGO Workflow]]`

## Что стоит раскрыть дальше

- [ ] Добавить базовый collect -> rebuild -> validate loop
- [ ] Уточнить, как profile data влияет на optimization decisions
- [ ] Проверить `related`
