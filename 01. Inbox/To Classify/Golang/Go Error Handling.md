---
aliases:
  - Error Handling in Go
  - Обработка ошибок в Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go]]"
  - "[[Go Interfaces]]"
  - "[[Go Testing]]"
tags: []
---

# Go Error Handling

## Краткое определение

Статья о том, как в Go устроена работа с ошибками через значения `error`, проверку, wrapping и error semantics.

## Основная идея или механизм

Go опирается на явную, value-based модель ошибок, в которой ошибка — часть контракта функции, а не скрытый побочный канал управления.

## Границы темы

- В тему входят `error`, wrapping, `errors.Is`, `errors.As` и idiomatic handling.
- На границе находится `[[Go Testing]]`, где error semantics уже проверяются тестами.

## Связи с другими заметками

Родительская тема:

`[[Go]]`

Связанные заметки:

- `[[Go Interfaces]]`
- `[[Go Testing]]`

## Примеры, случаи или следствия

В Go часто важна не строка ошибки сама по себе, а её программная семантика и корректная проверка на уровне API.

## Что стоит раскрыть дальше

- [ ] Добавить idioms wrapping and unwrapping
- [ ] Уточнить границы между errors и panic
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
