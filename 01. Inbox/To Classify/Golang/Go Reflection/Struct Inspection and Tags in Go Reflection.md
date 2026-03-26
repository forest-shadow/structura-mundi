---
aliases:
  - Struct Inspection in Go Reflection
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Addressability and Settable Values in Go Reflection]]"
  - "[[Reflection and Dynamic Decoding in Go]]"
  - "[[Go Composite Types]]"
tags: []
---

# Struct Inspection and Tags in Go Reflection

## Краткое определение

Статья о том, как reflection в Go используется для анализа структур, их полей и struct tags, включая связь этой техники со стандартными библиотеками вроде `encoding/json`.

## Основная идея или механизм

Во многих прикладных сценариях reflection в Go сводится к обходу `struct`-значений. Через `Kind()`, `NumField`, `Field`, `FieldByName`, `StructField` и `Tag.Get` язык позволяет читать метаданные полей и использовать их для сериализации, валидации и динамического маппинга.

## Границы темы

- В тему входят проверка на `Struct`, работа с `*struct`, чтение exported/unexported fields и struct tags.
- На границе находятся фактические mutation-операции и полное динамическое декодирование, которые лучше раскрывать отдельно.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[Addressability and Settable Values in Go Reflection]]`
- `[[Reflection and Dynamic Decoding in Go]]`
- `[[Dynamic Operations in Go Reflection]]`

## Примеры, случаи или следствия

- `encoding/json` и похожие инструменты опираются именно на структуру полей и теги, а не только на грубую типовую категорию значения.
- Различие между exported и unexported fields в reflection становится не просто стилевым, а runtime-ограничением доступа.

## Что стоит раскрыть дальше

- [ ] Добавить роль `StructField` и embedded fields
- [ ] Уточнить связь с `encoding/json`
- [ ] Проверить `related`
