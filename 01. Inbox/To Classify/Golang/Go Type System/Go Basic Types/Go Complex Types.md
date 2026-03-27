---
aliases:
  - Complex Number Types in Go
  - Complex Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Basic Types]]"
status: seed
related:
  - "[[Go Basic Types]]"
  - "[[Go Floating-Point Types]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Complex Types

## Краткое определение

Статья о типах `complex64` и `complex128` в Go как отдельном basic numeric family, построенном поверх вещественных компонентов.

## Основная идея или механизм

Complex types завершают numeric branch basic types в Go. Они не сводятся просто к паре float values на уровне типовой системы, а образуют отдельные predeclared basic types со своей операционной семантикой.

## Границы темы

- В тему входят `complex64`, `complex128` и их место среди basic numeric types.
- На границе находятся floating-point components, функции стандартной библиотеки и более широкая численная математика.

## Связи с другими заметками

Родительская тема:

`[[Go Basic Types]]`

Связанные заметки:

- `[[Go Floating-Point Types]]`
- `[[Go Assignability and Conversions]]`
- `[[Go Defined Types and Underlying Types]]`

## Примеры, случаи или следствия

- `complex64` и `complex128` логично читать после floating-point types, потому что они опираются на вещественный слой.
- Наличие отдельного complex family показывает, что numeric branch в Go не исчерпывается integer и float types.

## Что стоит раскрыть дальше

- [ ] Уточнить связь complex types с float components
- [ ] Добавить различие между `complex64` и `complex128`
- [ ] Проверить `related`
