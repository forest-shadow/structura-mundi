---
aliases:
  - Slice Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Array Types]]"
  - "[[Go Memory Management]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Slice Types

## Краткое определение

Статья о slice types в Go как о типах дескриптора динамической последовательности поверх массива.

## Основная идея или механизм

Slice type задается literal form `[]T` и представляет не сам массив, а описатель доступа к последовательности элементов. Поэтому slices нужно понимать отдельно от arrays, несмотря на их общую основу.

## Границы темы

- В тему входят slice types, их descriptor nature и связь с arrays.
- На границе находятся allocation behavior, append growth и memory aliasing.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Array Types]]`
- `[[Go Memory Management]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- Передача slice value не копирует весь underlying array, но меняет semantics shared access.
- Slice type часто выглядит как динамический массив, хотя типовая модель Go формулирует его иначе.

## Что стоит раскрыть дальше

- [ ] Уточнить descriptor model slice values
- [ ] Добавить связь с arrays и aliasing
- [ ] Проверить `related`
