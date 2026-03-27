---
aliases:
  - Boolean Type in Go
  - bool in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Basic Types]]"
status: seed
related:
  - "[[Go Basic Types]]"
  - "[[Go String Type]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Boolean Type

## Краткое определение

Статья о типе `bool` в Go как о единственном булевом basic type языка и о том, как он задает слой логических значений и условий.

## Основная идея или механизм

В Go булевы значения не смешиваются неявно с числами или строками: `bool` образует отдельный типовой класс, который используется в условиях, сравнениях и логических операциях.

## Границы темы

- В тему входят `bool`, булевы literals и логические операции.
- На границе находятся control-flow конструкции и сравнения как синтаксис программ, а не как свойства самого типа.

## Связи с другими заметками

Родительская тема:

`[[Go Basic Types]]`

Связанные заметки:

- `[[Go String Type]]`
- `[[Go Assignability and Conversions]]`
- `[[Go Defined Types and Underlying Types]]`

## Примеры, случаи или следствия

- В Go нет truthiness в стиле JavaScript или Python: условие требует именно `bool`.
- Именно из-за отдельности `bool` не работают неявные переходы между логическими и числовыми значениями.

## Что стоит раскрыть дальше

- [ ] Уточнить роль `bool` в comparisons и conditions
- [ ] Добавить связь с zero value
- [ ] Проверить `related`
