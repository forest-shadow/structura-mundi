---
aliases:
  - Dynamic Decoding in Go via Reflection
  - Reflection and Dynamic Decoding in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Go Reflection Struct Inspection and Tags]]"
  - "[[Go Reflection Mutation and Dynamic Calls]]"
  - "[[Go Reflection vs Generics vs Code Generation]]"
tags: []
---

# Go Reflection Dynamic Decoding

## Краткое определение

Статья о том, как reflection в Go используется для динамического декодирования структур данных и runtime-конверсии значений, особенно на границе с `any`, `map[string]any`, JSON-представлениями и рекурсивным заполнением структур.

## Основная идея или механизм

Dynamic decoding превращает reflection из абстрактного API в инженерный инструмент: программа получает слабо типизированные данные и пытается привести их к ожидаемой структуре через runtime-inspection, рекурсию и controlled mutation.

## Границы темы

- В тему входят `json.Unmarshal` в `any`, `map[string]any`, `[]any`, рекурсивная конвертация и заполнение структур через reflection.
- На границе находятся общие mutation-primitives и более широкий архитектурный выбор между reflection, generics и code generation.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[Go Reflection Struct Inspection and Tags]]`
- `[[Go Reflection Mutation and Dynamic Calls]]`
- `[[Go Reflection vs Generics vs Code Generation]]`

## Примеры, случаи или следствия

- Слабо типизированные JSON-данные часто попадают в программу как `map[string]any` и требуют отдельного слоя преобразования.
- Dynamic decoding делает особенно заметными ошибки в type assumptions, exported access и error-policy.

## Что стоит раскрыть дальше

- [ ] Добавить архитектурный разбор runtime conversion pipeline
- [ ] Уточнить политику ошибок и рекурсивное преобразование
- [ ] Проверить `related`
