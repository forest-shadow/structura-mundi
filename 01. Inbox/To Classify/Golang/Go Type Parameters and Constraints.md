---
aliases:
  - Type Parameters and Constraints in Go
  - Параметры типов и constraints в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Interfaces]]"
  - "[[Go Defined Types and Underlying Types]]"
tags: []
---

# Go Type Parameters and Constraints

## Краткое определение

Статья о parametric polymorphism в Go: type parameters, constraints и том, как язык выражает generic-код без отказа от своей общей простоты.

## Границы темы

- В тему входят generic declarations, type parameters и constraints как часть современной типовой системы Go.
- На границе находятся `[[Go Interfaces]]`, потому что constraints во многом выражаются через interface-like forms, но семантически не сводятся к обычным runtime interfaces.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Interfaces]]`
- `[[Go Defined Types and Underlying Types]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- Generics расширяют выразительность Go, но продолжают опираться на существующие правила identity и assignability.
- Constraints помогают описывать допустимые семейства типов без введения классической объектной иерархии.

## Что стоит раскрыть дальше

- [ ] Уточнить границы между ordinary interfaces и constraints
- [ ] Добавить типичные случаи, где generics действительно оправданы
- [ ] Проверить `aliases`
