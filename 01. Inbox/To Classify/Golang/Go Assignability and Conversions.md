---
aliases:
  - Assignability and Conversions in Go
  - Присваиваемость и преобразования в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Defined Types and Underlying Types]]"
  - "[[Go Interfaces]]"
tags: []
---

# Go Assignability and Conversions

## Краткое определение

Статья о правилах assignability и conversion в Go: когда значение можно использовать как есть, а когда требуется явное преобразование типа.

## Границы темы

- В тему входят типовая совместимость значений, присваивание, передача аргументов и явные conversions.
- На границе находятся `[[Go Interfaces]]`, потому что interface compatibility частично выражается через assignability rules.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Defined Types and Underlying Types]]`
- `[[Go Interfaces]]`
- `[[Go Methods and Method Sets]]`

## Примеры, случаи или следствия

- Одинаковая структура значений еще не гарантирует свободное присваивание между разными defined types.
- Явная conversion в Go обычно делает переход между типами намеренным, а не неявным.

## Что стоит раскрыть дальше

- [ ] Уточнить место type assertions на границе темы
- [ ] Добавить связь с untyped constants
- [ ] Проверить `aliases`
