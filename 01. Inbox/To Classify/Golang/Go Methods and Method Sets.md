---
aliases:
  - Methods and Method Sets in Go
  - Методы и method sets в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Interfaces]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Methods and Method Sets

## Краткое определение

Статья о том, как в Go методы прикрепляются к типам и как method sets определяют, какое поведение тип может предъявить напрямую или через интерфейсную совместимость.

## Границы темы

- В тему входят receivers, method sets и их влияние на interface implementation.
- На границе находятся `[[Go Interfaces]]`, где method sets становятся практическим механизмом structural typing.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Interfaces]]`
- `[[Go Defined Types and Underlying Types]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- Различие между value receiver и pointer receiver меняет method set типа и влияет на interface satisfaction.
- Именно method sets объясняют, почему один и тот же struct type может вести себя по-разному в разных контекстах использования.

## Что стоит раскрыть дальше

- [ ] Уточнить границы между methods, receivers и interface satisfaction
- [ ] Добавить связь с pointer semantics
- [ ] Проверить `aliases`
