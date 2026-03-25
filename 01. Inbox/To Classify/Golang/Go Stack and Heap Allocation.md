---
aliases:
  - Stack and Heap Allocation in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Memory Management]]"
status: seed
related:
  - "[[Go Memory Management]]"
  - "[[Go Escape Analysis]]"
tags: []
---

# Go Stack and Heap Allocation

## Краткое определение

Статья о том, как в Go различаются стековое и кучное размещение значений и почему это различие важно для стоимости исполнения программы.

## Основная идея или механизм

В Go часть значений может жить на стеке текущей goroutine, а часть размещается в куче. Это влияет на стоимость аллокаций, pressure на GC и поведение горячих путей исполнения.

## Границы темы

- В тему входят stack vs heap placement, lifetime значений и практические следствия для производительности.
- На границе находятся `[[Go Escape Analysis]]` как механизм решения компилятора и `[[Go Garbage Collection]]` как тема reclaiming heap memory.

## Связи с другими заметками

Родительская тема:

`[[Go Memory Management]]`

Связанные заметки:

- `[[Go Escape Analysis]]`
- `[[Go Garbage Collection]]`

## Примеры, случаи или следствия

- Значения на стеке обычно дешевле в управлении, потому что не требуют участия GC.
- Heap allocation сама по себе не всегда плоха, но её частота начинает иметь значение на hot path.
- Одна и та же логическая структура данных может попадать либо в stack, либо в heap в зависимости от ее использования.

## Что стоит раскрыть дальше

- [ ] Уточнить, как растет стек goroutine
- [ ] Добавить примеры stack-to-heap transitions
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
