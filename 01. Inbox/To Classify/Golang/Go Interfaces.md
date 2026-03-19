---
aliases:
  - Interfaces in Go
  - Интерфейсы Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go]]"
  - "[[Go Type System]]"
  - "[[Go Error Handling]]"
tags: []
---

# Go Interfaces

## Краткое определение

Статья о том, как в Go работают интерфейсы как механизм абстракции и совместимости типов.

## Основная идея или механизм

Интерфейсы в Go опираются на structural typing и реализуются не через явную декларацию, а через соответствие набора методов.

## Границы темы

- В тему входят interface values, method sets и идиома small interfaces.
- На границе находится `[[Go Type System]]`, где контекст шире, чем сами интерфейсы.

## Связи с другими заметками

Родительская тема:

`[[Go]]`

Связанные заметки:

- `[[Go Type System]]`
- `[[Go Error Handling]]`

## Примеры, случаи или следствия

В Go интерфейс чаще описывает минимальный поведенческий контракт, а не часть глубокой объектной иерархии.

## Что стоит раскрыть дальше

- [ ] Добавить различие empty interface и typed interfaces
- [ ] Уточнить idiomatic use of small interfaces
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
