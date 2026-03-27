---
aliases:
  - Floating Point Types in Go
  - Float Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Basic Types]]"
status: seed
related:
  - "[[Go Basic Types]]"
  - "[[Go Integer Types]]"
  - "[[Go Complex Types]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Floating-Point Types

## Краткое определение

Статья о типах `float32` и `float64` в Go как отдельном семействе basic numeric types с собственными правилами точности и вычислительного поведения.

## Основная идея или механизм

Floating-point types в Go задают вещественный слой numeric model языка. Они ближе к complex types, чем к integer families, но сохраняют собственную семантику точности, представления и вычислений.

## Границы темы

- В тему входят `float32`, `float64` и их роль как basic numeric types.
- На границе находятся untyped floating constants, conversions и использование float-компонент внутри complex values.

## Связи с другими заметками

Родительская тема:

`[[Go Basic Types]]`

Связанные заметки:

- `[[Go Integer Types]]`
- `[[Go Complex Types]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- Различие между `float32` и `float64` важно не только для памяти, но и для точности вычислений.
- Floating-point types естественно связывают integer layer с complex layer.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между `float32` и `float64`
- [ ] Добавить связь с complex components
- [ ] Проверить `related`
