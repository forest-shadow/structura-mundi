---
aliases:
  - Defined Types and Underlying Types in Go
  - Именованные и underlying types в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Basic Types]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Defined Types and Underlying Types

## Краткое определение

Статья о том, как в Go соотносятся defined types, их underlying types и типовая идентичность, которая не равна одной лишь форме представления значения.

## Границы темы

- В тему входят named types, их связь с existing representations и последствия для identity.
- На границе находятся `[[Go Assignability and Conversions]]`, где эти различия превращаются в практические правила совместимости.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Basic Types]]`
- `[[Go Assignability and Conversions]]`
- `[[Go Type Parameters and Constraints]]`

## Примеры, случаи или следствия

- Два типа могут иметь похожую структуру, но оставаться разными defined types и поэтому не быть свободно взаимозаменяемыми.
- Understanding underlying types помогает объяснить, когда conversion возможна, а когда типовая идентичность все еще различает значения.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между defined types и aliases
- [ ] Добавить связь с method sets
- [ ] Проверить `aliases`
