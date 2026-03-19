---
aliases:
  - Goroutines
  - Горутины Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Concurrency Model]]"
status: draft
related:
  - "[[Go]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Channels]]"
  - "[[Go Scheduler]]"
tags: []
---

# Go Goroutines

## Краткое определение

Статья о goroutines как основном механизме конкурентного запуска функций в Go.

## Основная идея или механизм

Goroutine — это лёгкая единица конкурентного выполнения, управляемая рантаймом Go и позволяющая строить concurrency без прямой работы с тяжёлыми системными потоками на уровне исходного кода.

## Границы темы

- В тему входят запуск, жизненный цикл и практическая роль goroutines.
- На границе находятся `[[Go Channels]]`, `[[Go Scheduler]]` и синхронизационные примитивы.

## Связи с другими заметками

Родительская тема:

`[[Go Concurrency Model]]`

Связанные заметки:

- `[[Go Channels]]`
- `[[Go Scheduler]]`
- `[[Go]]`

## Примеры, случаи или следствия

В Go конкурентность обычно выражается не в ручном управлении потоками, а в запуске goroutines и последующей координации их работы.

## Что стоит раскрыть дальше

- [ ] Уточнить роль scheduler
- [ ] Добавить практические caveats про leaks
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
