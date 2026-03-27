---
aliases:
  - Function Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Type Literals]]"
  - "[[Go Interfaces]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Function Types

## Краткое определение

Статья о function types в Go как о типах, определяемых сигнатурой параметров и результатов.

## Основная идея или механизм

Function type задается literal form `func(...) ...` и определяет callable shape значения. В Go функция является значением, но ее type identity определяется именно сигнатурой.

## Границы темы

- В тему входят function types, signatures и callable values.
- На границе находятся closures, method values и interface-based abstraction поверх функций.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Type Literals]]`
- `[[Go Interfaces]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- Две функции совпадают по типу только тогда, когда совпадает их сигнатура в терминах параметров и результатов.
- Function types важны как для прямого вызова, так и для callback-style APIs.

## Что стоит раскрыть дальше

- [ ] Уточнить связь function types и closures
- [ ] Добавить границу с methods и interfaces
- [ ] Проверить `related`
