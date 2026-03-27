---
aliases:
  - Interfaces in Go
  - Интерфейсы Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: draft
related:
  - "[[Go]]"
  - "[[Go Type System]]"
  - "[[Go Methods and Method Sets]]"
  - "[[Go Error Handling]]"
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

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go]]`
- `[[Go Methods and Method Sets]]`
- `[[Go Assignability and Conversions]]`
- `[[Go Error Handling]]`

## Примеры, случаи или следствия

В Go интерфейс чаще описывает минимальный поведенческий контракт, а не часть глубокой объектной иерархии.

## Что стоит раскрыть дальше

- [ ] Добавить различие empty interface и typed interfaces
- [ ] Уточнить idiomatic use of small interfaces
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
