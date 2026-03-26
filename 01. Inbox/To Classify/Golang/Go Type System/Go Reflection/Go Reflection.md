---
aliases:
  - Reflection in Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Interfaces]]"
  - "[[reflect.Type, reflect.Value and reflect.Kind]]"
  - "[[Addressability and Settable Values in Go Reflection]]"
  - "[[Reflection vs Generics vs Code Generation in Go]]"
tags: []
---

# Go Reflection

## Краткое определение области

`Go Reflection` — это обзорная заметка о механизме runtime-инспекции и ограниченной динамической работы со значениями и типами в Go. Она задает карту темы: что именно reflection видит в runtime, зачем она существует, где проходят ее границы и какие отдельные статьи раскрывают фундамент, ограничения, практические сценарии и архитектурные trade-offs.

## Что входит в эту тему

- `[[reflect.Type, reflect.Value and reflect.Kind]]`
- `[[Addressability and Settable Values in Go Reflection]]`
- `[[Struct Inspection and Tags in Go Reflection]]`
- `[[Dynamic Operations in Go Reflection]]`
- `[[Reflection and Dynamic Decoding in Go]]`
- `[[Reflection vs Generics vs Code Generation in Go]]`
- `[[Performance and Limits of Go Reflection]]`

## Как устроена ветка

- `reflect.Type, reflect.Value and reflect.Kind` задает понятийный фундамент всей ветки и объясняет, какие runtime-объекты предоставляет пакет `reflect`.
- `Addressability and Settable Values in Go Reflection` фиксирует главный слой ограничений reflection и объясняет, почему чтение и изменение значений в runtime подчиняются разным правилам.
- `Struct Inspection and Tags in Go Reflection` собирает наиболее частый прикладной случай: анализ структур, полей и тегов.
- `Dynamic Operations in Go Reflection` показывает, как reflection переходит от инспекции к созданию, изменению и вызовам.
- `Reflection and Dynamic Decoding in Go` выносит reflection в самостоятельный инженерный кейс, где она используется для runtime-конверсии и построения динамического декодирования.
- `Reflection vs Generics vs Code Generation in Go` и `Performance and Limits of Go Reflection` завершают ветку архитектурной и инженерной оценкой подхода.

## Рекомендуемый маршрут чтения

1. Начать с `[[reflect.Type, reflect.Value and reflect.Kind]]`.
2. Затем перейти к `[[Addressability and Settable Values in Go Reflection]]`.
3. После этого читать `[[Struct Inspection and Tags in Go Reflection]]` и `[[Dynamic Operations in Go Reflection]]`.
4. Затем перейти к `[[Reflection and Dynamic Decoding in Go]]` как к прикладному кейсу.
5. Завершить `[[Reflection vs Generics vs Code Generation in Go]]` и `[[Performance and Limits of Go Reflection]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Go Type System]]`
- `[[Go Memory Management]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные статьи про `Go Type Assertions` и `Empty Interface and any in Go`
- [ ] Проверить, нужен ли отдельный article про `Reflection Safety Patterns in Go`
- [ ] Проверить `related`
