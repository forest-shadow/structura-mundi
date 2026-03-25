---
aliases:
  - Garbage Collection in Go
  - Go GC
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Memory Management]]"
status: seed
related:
  - "[[Go Memory Management]]"
  - "[[Go Escape Analysis]]"
  - "[[Go Scheduler]]"
tags: []
---

# Go Garbage Collection

## Краткое определение

Статья о сборщике мусора Go как части runtime, которая освобождает недостижимую heap memory и влияет на latency, throughput и allocation strategy.

## Основная идея или механизм

GC в Go нужен потому, что heap memory не освобождается автоматически по выходу из stack frame. Поэтому runtime отслеживает достижимость объектов, выполняет фазы сборки и старается удерживать паузы приемлемыми для production workloads.

## Границы темы

- В тему входят heap objects, GC pressure, pausing behavior, background work и практические следствия для производительности.
- На границе находятся `[[Go Escape Analysis]]`, который влияет на частоту heap allocations, и `[[Go Scheduler]]`, внутри которого GC тоже выполняет часть фоновой работы.

## Связи с другими заметками

Родительская тема:

`[[Go Memory Management]]`

Связанные заметки:

- `[[Go Escape Analysis]]`
- `[[Go Scheduler]]`

## Примеры, случаи или следствия

- Высокая частота heap allocations повышает GC pressure даже без изменения бизнес-логики программы.
- Хорошая latency в Go не означает, что память можно игнорировать: allocation rate по-прежнему критичен для high-load систем.
- GC behavior полезно анализировать вместе с профилированием, а не изолированно.

## Что стоит раскрыть дальше

- [ ] Добавить базовую карту фаз GC
- [ ] Уточнить связь с write barriers и scheduler
- [ ] Добавить operational heuristics для чтения memory profiles
- [ ] Проверить `aliases`
