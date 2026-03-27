---
aliases:
  - Array Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Type Literals]]"
  - "[[Go Slice Types]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Array Types

## Краткое определение

Статья о массивах в Go как о типах фиксированной последовательности элементов, где длина входит в сам тип.

## Основная идея или механизм

Array type в Go определяется literal form `[N]T`. Это означает, что размер массива является частью type identity, а сами arrays ведут себя не так, как slices, несмотря на тесную связь между ними.

## Границы темы

- В тему входят array types, их fixed length и различие между `[N]T` и `[]T`.
- На границе находятся slices, conversions и вопросы размещения в памяти.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Type Literals]]`
- `[[Go Slice Types]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- `[4]int` и `[8]int` в Go являются разными типами, а не значениями одного контейнерного класса.
- Arrays часто служат основой для slices, но не совпадают с ними по семантике передачи и identity.

## Что стоит раскрыть дальше

- [ ] Уточнить связь array types и slices
- [ ] Добавить роль длины как части типа
- [ ] Проверить `related`
