---
aliases:
  - Type Literals in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Defined Types and Underlying Types]]"
  - "[[Go Array Types]]"
  - "[[Go Interfaces]]"
tags: []
---

# Go Type Literals

## Краткое определение

Статья о type literals в Go: формах типов, которые задаются структурой самого типа, а не его именем.

## Основная идея или механизм

Composite branch в Go строится вокруг literal forms вроде `[N]T`, `struct{...}`, `*T`, `func(...)`, `interface{...}`, `[]T`, `map[K]V` и `chan T`. Именно literal shape задает, к какому семейству относится тип и какие свойства он получает.

## Границы темы

- В тему входят type literals как общий принцип задания composite types.
- На границе находятся defined types, которые получают имя поверх уже существующего literal-based underlying type.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Defined Types and Underlying Types]]`
- `[[Go Array Types]]`
- `[[Go Interfaces]]`

## Примеры, случаи или следствия

- Два defined types могут опираться на один и тот же structural literal, но оставаться разными по identity.
- Именно через type literals в Go выражается большинство небазовых форм данных и поведения.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между type literals и underlying types
- [ ] Добавить полный обзор literal forms
- [ ] Проверить `related`
