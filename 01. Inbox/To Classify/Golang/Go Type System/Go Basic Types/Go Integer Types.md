---
aliases:
  - Integer Types in Go
  - Integers in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Basic Types]]"
status: seed
related:
  - "[[Go Basic Types]]"
  - "[[Go Floating-Point Types]]"
  - "[[Go Defined Types and Underlying Types]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Integer Types

## Краткое определение

Статья о целочисленных basic types в Go: signed и unsigned integer families, platform-dependent типах `int` и `uint`, fixed-width integer types и alias-именах `byte` и `rune`.

## Основная идея или механизм

Целочисленный слой Go организован не как перечень несвязанных builtin names, а как несколько устойчивых подгрупп. Внутри одной статьи удобно удерживать различие между platform-dependent integer types, fixed-width integer types и alias-именами, не распадаясь на десяток мелких notes.

## Границы темы

- В тему входят `int`, `uint`, `uintptr`, `int8/16/32/64`, `uint8/16/32/64`, а также `byte` и `rune`.
- На границе находятся untyped constants, overflow semantics, pointer arithmetic constraints и conversions как отдельные аспекты типовой системы.

## Связи с другими заметками

Родительская тема:

`[[Go Basic Types]]`

Связанные заметки:

- `[[Go Floating-Point Types]]`
- `[[Go Defined Types and Underlying Types]]`
- `[[Go Assignability and Conversions]]`

## Примеры, случаи или следствия

- `int` и `uint` зависят от платформы и поэтому не заменяют fixed-width integer types в протоколах и форматах данных.
- `byte` и `rune` не образуют отдельные базовые семейства, а служат alias-именами внутри integer layer.

## Что стоит раскрыть дальше

- [ ] Развести platform-dependent и fixed-width integer types
- [ ] Добавить роль `uintptr`, `byte` и `rune`
- [ ] Проверить границу с untyped constants
