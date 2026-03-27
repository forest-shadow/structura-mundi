---
aliases:
  - Basic Types in Go
  - Базовые типы Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Composite Types]]"
  - "[[Go Defined Types and Underlying Types]]"
  - "[[Go Integer Types]]"
tags: []
---

# Go Basic Types

## Краткое определение области

`Go Basic Types` — это обзорная заметка о минимальном слое типовой системы Go: булевых значениях, строках и числовых типах, с которых начинается работа языка с данными. Она задает карту темы и разводит семейства basic types, не превращая ветку в плоский список заметок про каждый builtin по отдельности.

## Что входит в эту тему

- `[[Go Boolean Type]]`
- `[[Go String Type]]`
- `[[Go Integer Types]]`
- `[[Go Floating-Point Types]]`
- `[[Go Complex Types]]`

## Как устроена ветка

- `Go Boolean Type` фиксирует единственный булев тип Go и его границы: в языке нет числовой truthiness и неявных логических преобразований.
- `Go String Type` собирает свойства строк как basic type, а также их связь с байтами, рунами и текстовым представлением.
- `Go Integer Types` объединяет signed и unsigned integer family, включая platform-dependent типы `int` и `uint`, fixed-width типы и alias-имена `byte` и `rune`.
- `Go Floating-Point Types` описывает `float32` и `float64` как отдельное числовое семейство.
- `Go Complex Types` завершает numeric cluster и связывает complex values с их floating-point основой.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Boolean Type]]` и `[[Go String Type]]`, чтобы зафиксировать небезчисловые basic types.
2. Затем перейти к `[[Go Integer Types]]` как к самому разветвленному семейству базовых типов.
3. После этого читать `[[Go Floating-Point Types]]` и `[[Go Complex Types]]`.
4. Затем перейти к `[[Go Composite Types]]`, чтобы увидеть, как язык строит более сложные формы данных поверх basic types.
5. После этого сопоставить ветку с `[[Go Defined Types and Underlying Types]]` и `[[Go Assignability and Conversions]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Go Type System]]`
- `[[Go Reflection]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позднее отдельный article про untyped constants и default types в Go
- [ ] Проверить, когда внутри `Go Integer Types` понадобятся отдельные notes про integer overflow semantics или `uintptr`
- [ ] Проверить `related`
