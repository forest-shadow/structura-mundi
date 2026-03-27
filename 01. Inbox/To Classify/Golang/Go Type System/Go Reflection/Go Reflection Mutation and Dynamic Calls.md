---
aliases:
  - Dynamic Mutation in Go Reflection
  - Dynamic Operations in Go Reflection
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Go Reflection Addressability and Settable Values]]"
  - "[[Go Reflection Struct Inspection and Tags]]"
  - "[[Go Reflection Performance and Limits]]"
tags: []
---

# Go Reflection Mutation and Dynamic Calls

## Краткое определение

Статья о том, как reflection в Go не только читает runtime-данные, но и создает значения, изменяет их и вызывает методы динамически.

## Основная идея или механизм

Этот слой reflection начинается там, где программа перестает быть только наблюдателем runtime-структуры и начинает действовать над ней через `Set`, `SetInt`, `SetString`, `MakeSlice`, `MakeMap`, `MethodByName` и `Call`. Именно здесь особенно заметны проверки, ограничения и риск panic.

## Границы темы

- В тему входят mutation-операции, создание новых значений, динамический вызов методов и базовые требования к аргументам.
- На границе находится полноценное прикладное декодирование и архитектурная оценка reflection как подхода.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[Go Reflection Addressability and Settable Values]]`
- `[[Go Reflection Struct Inspection and Tags]]`
- `[[Go Reflection Performance and Limits]]`

## Примеры, случаи или следствия

- Dynamic operations особенно полезны в инфраструктурном коде, где тип заранее неизвестен, но за это приходится платить runtime-проверками.
- Большая часть опасности reflection проявляется не в чтении метаданных, а именно в mutation и `Call`.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между `Set*` и `CanSet`
- [ ] Решить, нужен ли позже отдельный article про dynamic method calls
- [ ] Проверить `related`
