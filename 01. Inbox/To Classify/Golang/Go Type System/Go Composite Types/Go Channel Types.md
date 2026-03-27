---
aliases:
  - Channel Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Composite Types]]"
  - "[[Go Type Literals]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Channels]]"
tags: []
---

# Go Channel Types

## Краткое определение

Статья о channel types в Go как о типах типизированной передачи значений между goroutines.

## Основная идея или механизм

Channel type задается literal form `chan T`, `<-chan T` или `chan<- T` и объединяет type-level описание потока значений с concurrency semantics. Поэтому channel types находятся на границе между type system и concurrency model.

## Границы темы

- В тему входят channel types, directionality и типизированная передача значений.
- На границе находятся scheduler behavior, blocking semantics и более широкая concurrency coordination.

## Связи с другими заметками

Родительская тема:

`[[Go Composite Types]]`

Связанные заметки:

- `[[Go Type Literals]]`
- `[[Go Concurrency Model]]`
- `[[Go Channels]]`

## Примеры, случаи или следствия

- Directional channel types показывают, что часть ограничений канала задается уже на уровне типа.
- Channel types — один из самых явных примеров пересечения типовой системы и concurrency semantics в Go.

## Что стоит раскрыть дальше

- [ ] Уточнить связь channel types с directional forms
- [ ] Добавить границу между type-level и runtime-level behavior каналов
- [ ] Проверить `related`
