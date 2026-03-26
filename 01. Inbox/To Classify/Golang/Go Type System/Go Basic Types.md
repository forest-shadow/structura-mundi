---
aliases:
  - Basic Types in Go
  - Базовые типы Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Composite Types]]"
  - "[[Go Defined Types and Underlying Types]]"
tags: []
---

# Go Basic Types

## Краткое определение

Статья о базовых типах Go: числах, булевых значениях, строках и других предопределенных формах данных, с которых начинается типовая модель языка.

## Границы темы

- В тему входят predeclared basic types и их роль как минимального типового слоя языка.
- На границе находятся `[[Go Composite Types]]`, где из базовых значений уже собираются более сложные формы данных.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Composite Types]]`
- `[[Go Defined Types and Underlying Types]]`

## Примеры, случаи или следствия

- Именно basic types задают базовые операции и literals, от которых строится остальная типовая семантика.
- Многие defined types в Go возникают как новые имена поверх уже существующих basic types.

## Что стоит раскрыть дальше

- [ ] Добавить различие между numeric, boolean и string types
- [ ] Уточнить роль untyped constants на границе темы
- [ ] Проверить `aliases`
