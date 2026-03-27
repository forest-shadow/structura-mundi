---
aliases:
  - String Type in Go
  - string in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Basic Types]]"
status: seed
related:
  - "[[Go Basic Types]]"
  - "[[Go Integer Types]]"
  - "[[Go Composite Types]]"
tags: []
---

# Go String Type

## Краткое определение

Статья о типе `string` в Go как о basic type для текстовых и байтовых последовательностей и о его связи с литералами, immutability и текстовым представлением.

## Основная идея или механизм

`string` в Go является basic type, но при этом тесно связан с байтами и рунами. Это делает его пограничной темой между минимальным типовым слоем языка и более прикладными вопросами текстовой обработки.

## Границы темы

- В тему входят `string`, string literals, immutability и связь строк с `byte` и `rune`.
- На границе находятся срезы байтов, работа с UTF-8 и более общая текстовая обработка.

## Связи с другими заметками

Родительская тема:

`[[Go Basic Types]]`

Связанные заметки:

- `[[Go Integer Types]]`
- `[[Go Composite Types]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- Строка в Go не является массивом символов в языковом смысле, хотя часто интерпретируется как текст.
- Связь `string` с `byte` и `rune` делает эту тему важной для чтения API и понимания literals.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между `string`, `byte` и `rune`
- [ ] Добавить границу между `string` и `[]byte`
- [ ] Проверить `related`
