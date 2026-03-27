---
aliases:
  - Pointer Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Type Literals]]"
  - "[[Go Memory Management]]"
  - "[[Go Methods and Method Sets]]"
tags: []
---

# Go Pointer Types

## Краткое определение

Статья об указательных типах в Go как о типах адреса значения определенного базового или составного типа.

## Основная идея или механизм

Pointer type задается literal form `*T` и выражает доступ к значению через адрес. В Go указатели тесно связаны с method sets, zero values и behavior around allocation, но не дают общей арифметики указателей как в C.

## Границы темы

- В тему входят pointer types, `*T`, zero value pointers и различие между значением и ссылкой на значение.
- На границе находятся escape analysis, allocation behavior и addressability в reflection.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Type Literals]]`
- `[[Go Memory Management]]`
- `[[Go Methods and Method Sets]]`

## Примеры, случаи или следствия

- Pointer receivers и pointer values меняют то, какие методы видны у типа.
- Указатели в Go важны для semantics shared state, но подчиняются более строгой модели, чем в системных языках с pointer arithmetic.

## Что стоит раскрыть дальше

- [ ] Уточнить связь pointer types с method sets
- [ ] Добавить границу с memory-management notes
- [ ] Проверить `related`
