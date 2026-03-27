---
aliases:
  - Composite Types in Go
  - Составные типы Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Basic Types]]"
  - "[[Go Interfaces]]"
  - "[[Go Memory Management]]"
tags: []
---

# Go Composite Types

## Краткое определение области

`Go Composite Types` — это обзорная заметка о типах Go, задаваемых type literals: массивах, структурах, указателях, функциях, интерфейсах, срезах, map и каналах. Она задает карту этой ветки и раскладывает composite types по устойчивым семействам, а не оставляет их длинным плоским списком builtin form-паттернов.

## Что входит в эту тему

- `[[Go Type Literals]]`
- `[[Go Array Types]]`
- `[[Go Struct Types]]`
- `[[Go Pointer Types]]`
- `[[Go Function Types]]`
- `[[Go Interfaces]]`
- `[[Go Slice Types]]`
- `[[Go Map Types]]`
- `[[Go Channel Types]]`

## Как устроена ветка

- `Go Type Literals` дает общий фундамент для всей ветки и объясняет, почему composite types в Go задаются не именем, а literal form типа.
- `Go Array Types` и `Go Struct Types` собирают фиксированные составные формы, где структура значения входит в сам тип.
- `Go Pointer Types` и `Go Function Types` описывают composite forms, которые не являются контейнерами, но задают отдельные способы адресации и вызова.
- `Go Interfaces` остаются внутри этой ветки как особый composite/type-literal узел, где тип определяется методами, а в generic-контексте также type sets.
- `Go Slice Types`, `Go Map Types` и `Go Channel Types` собирают runtime-backed формы, наиболее тесно связанные с allocation behavior, aliasing и координацией.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Type Literals]]`.
2. Затем перейти к `[[Go Array Types]]` и `[[Go Struct Types]]`.
3. После этого читать `[[Go Pointer Types]]` и `[[Go Function Types]]`.
4. Затем перейти к `[[Go Interfaces]]` как к поведенческой и generic-aware форме composite type.
5. После этого читать `[[Go Slice Types]]`, `[[Go Map Types]]` и `[[Go Channel Types]]`.
6. Затем сопоставить ветку с `[[Go Memory Management]]`, `[[Go Methods and Method Sets]]` и `[[Go Assignability and Conversions]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Go Type System]]`
- `[[Go Basic Types]]`
- `[[Go Reflection]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позднее отдельный article про zero values composite types
- [ ] Проверить, когда `Go Slice Types` и `Go Map Types` потребуют собственных дочерних веток
- [ ] Проверить `related`
