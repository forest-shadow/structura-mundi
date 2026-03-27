---
aliases:
  - Map Types in Go
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
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Map Types

## Краткое определение

Статья о map types в Go как о типах ассоциативного отображения ключей в значения.

## Основная идея или механизм

Map type задается literal form `map[K]V` и выражает не record-like shape, а key-value relation с собственной runtime semantics. Это делает map отдельным семейством composite types, а не просто частным случаем container type.

## Границы темы

- В тему входят map types, key-value shape и различие между map и struct.
- На границе находятся hashing internals, concurrency safety и allocation behavior.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Type Literals]]`
- `[[Go Struct Types]]`
- `[[Go Memory Management]]`

## Примеры, случаи или следствия

- Выбор между map и struct в Go означает выбор между динамическим key set и фиксированной схемой полей.
- Map values тесно связаны с runtime behavior и поэтому их удобно читать рядом с memory notes.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между map types и struct types
- [ ] Добавить связь с runtime behavior и zero value
- [ ] Проверить `related`
