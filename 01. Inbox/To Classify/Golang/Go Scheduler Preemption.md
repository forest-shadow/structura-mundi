---
aliases:
  - Preemption in Go Scheduler
  - Go Preemption
  - Вытеснение в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler]]"
status: draft
related:
  - "[[Go Scheduler]]"
  - "[[Go Goroutines]]"
  - "[[Go Scheduler GMP Model]]"
tags: []
---

# Go Scheduler Preemption

## Краткое определение

Статья о preemption в Go как механизме, который позволяет рантайму возвращать управление и не допускать чрезмерного monopolization CPU одной goroutine.

## Основная идея или механизм

Preemption нужна для того, чтобы планировщик сохранял управляемость исполнения и fairness, даже если выполняемый код сам по себе долго не уступает управление.

## Границы темы

- В тему входят причины preemption и её роль в scheduler behavior.
- На границе находятся общие вопросы runtime internals и взаимодействия с GC.

## Связи с другими заметками

Родительская тема:

`[[Go Scheduler]]`

Связанные заметки:

- `[[Go Goroutines]]`
- `[[Go Scheduler GMP Model]]`

## Примеры, случаи или следствия

Без preemption долгий CPU-bound код может ухудшать responsiveness и мешать своевременному выполнению других goroutines.

## Что стоит раскрыть дальше

- [ ] Уточнить cooperative vs asynchronous preemption
- [ ] Добавить связь с GC safepoints
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
