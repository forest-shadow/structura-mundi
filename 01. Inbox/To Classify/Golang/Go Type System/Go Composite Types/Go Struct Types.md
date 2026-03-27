---
aliases:
  - Struct Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Type Literals]]"
  - "[[Go Methods and Method Sets]]"
  - "[[Go Defined Types and Underlying Types]]"
tags: []
---

# Go Struct Types

## Краткое определение

Статья о struct types в Go как о record-like типах с набором именованных полей.

## Основная идея или механизм

Struct type в Go задается literal form `struct{...}` и определяет фиксированную схему полей. Именно struct types часто становятся базой для domain modeling, methods и field-based composition.

## Границы темы

- В тему входят struct types, поля и field-based shape значения.
- На границе находятся методы, tags и reflection-based inspection.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Type Literals]]`
- `[[Go Methods and Method Sets]]`
- `[[Go Reflection Struct Inspection and Tags]]`

## Примеры, случаи или следствия

- Struct type задает форму записи, на которую затем могут навешиваться методы и defined-type semantics.
- Выбор между struct и map влияет не только на API, но и на устойчивость shape данных.

## Что стоит раскрыть дальше

- [ ] Уточнить связь struct types с methods и tags
- [ ] Добавить границу между struct types и map-based data
- [ ] Проверить `related`
