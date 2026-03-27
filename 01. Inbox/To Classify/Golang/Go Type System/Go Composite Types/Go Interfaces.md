---
aliases:
  - Interfaces in Go
  - Интерфейсы Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: draft
related:
  - "[[Go Composite Types]]"
  - "[[Go Type System]]"
  - "[[Go Type Literals]]"
  - "[[Go Methods and Method Sets]]"
  - "[[Go Type Parameters and Constraints]]"
tags: []
---

# Go Interfaces

## Краткое определение

Статья о том, как в Go работают интерфейсы как часть типовой системы, механизм абстракции и способ выражения совместимости типов.

## Основная идея или механизм

Интерфейсы в Go опираются на structural typing и реализуются не через явную декларацию, а через соответствие набора методов.

## Границы темы

- В тему входят interface values, method sets и идиома small interfaces.
- На границе находится `[[Go Type System]]`, где контекст шире, чем сами интерфейсы.
- Механический фундамент темы частично раскрывается в `[[Go Methods and Method Sets]]`.
- В generic-контексте граница темы расширяется до type sets и constraint-форм.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Composite Types]]`
- `[[Go Type Literals]]`
- `[[Go Methods and Method Sets]]`
- `[[Go Assignability and Conversions]]`
- `[[Go Type Parameters and Constraints]]`

## Примеры, случаи или следствия

В Go интерфейс чаще описывает минимальный поведенческий контракт, а не часть глубокой объектной иерархии.

## Что стоит раскрыть дальше

- [ ] Добавить различие между interface values, typed interfaces и constraints
- [ ] Уточнить idiomatic use of small interfaces
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
