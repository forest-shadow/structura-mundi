---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Translation Pipeline]]"
status: seed
related:
  - "[[Parsing]]"
  - "[[Abstract Syntax Tree]]"
  - "[[Intermediate Representation]]"
tags: []
---

# Semantic Analysis

## Краткое определение

`Semantic Analysis` — это стадия, на которой структурно корректная программа дополнительно проверяется на смысловые ограничения языка.

## Основная идея или механизм

Здесь обычно уточняются области видимости имен, типовые ограничения, корректность обращений и другие инварианты, которые нельзя проверить одной только грамматикой.

## Границы темы

- Входит: name resolution, type checking, semantic constraints.
- Не входит: чисто синтаксический parsing и machine-specific code generation.

## Связи с другими заметками

Родительская тема:

`[[Program Translation Pipeline]]`

Связанные заметки:

- `[[Parsing]]`
- `[[Abstract Syntax Tree]]`
- `[[Intermediate Representation]]`

## Примеры, случаи или следствия

Программа может быть syntactically valid, но semantically invalid, если имя не объявлено, типы несовместимы или нарушены ограничения языка на использование конструкции.

## Что стоит раскрыть дальше

- [ ] Уточнить различие semantic analysis и type checking
- [ ] Проверить роль symbol tables
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
