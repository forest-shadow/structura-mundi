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
  - "[[Go Reflection Type and Value Model]]"
  - "[[Go Reflection Addressability and Settable Values]]"
  - "[[Go Reflection vs Generics vs Code Generation]]"
tags: []
---

# Go Reflection

## Краткое определение области

`Go Reflection` — это обзорная заметка о механизме runtime-инспекции и ограниченной динамической работы со значениями и типами в Go. Она задает карту темы: что именно reflection видит в runtime, зачем она существует, где проходят ее границы и какие отдельные статьи раскрывают фундамент, ограничения, практические сценарии и архитектурные trade-offs.

## Что входит в эту тему

- `[[Go Reflection Type and Value Model]]`
- `[[Go Reflection Addressability and Settable Values]]`
- `[[Go Reflection Struct Inspection and Tags]]`
- `[[Go Reflection Mutation and Dynamic Calls]]`
- `[[Go Reflection Dynamic Decoding]]`
- `[[Go Reflection vs Generics vs Code Generation]]`
- `[[Go Reflection Performance and Limits]]`

## Как устроена ветка

- `Go Reflection Type and Value Model` задает понятийный фундамент всей ветки и объясняет, какие runtime-объекты предоставляет пакет `reflect`.
- `Go Reflection Addressability and Settable Values` фиксирует главный слой ограничений reflection и объясняет, почему чтение и изменение значений в runtime подчиняются разным правилам.
- `Go Reflection Struct Inspection and Tags` собирает наиболее частый прикладной случай: анализ структур, полей и тегов.
- `Go Reflection Mutation and Dynamic Calls` показывает, как reflection переходит от инспекции к созданию, изменению и вызовам.
- `Go Reflection Dynamic Decoding` выносит reflection в самостоятельный инженерный кейс, где она используется для runtime-конверсии и построения динамического декодирования.
- `Go Reflection vs Generics vs Code Generation` и `Go Reflection Performance and Limits` завершают ветку архитектурной и инженерной оценкой подхода.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Reflection Type and Value Model]]`.
2. Затем перейти к `[[Go Reflection Addressability and Settable Values]]`.
3. После этого читать `[[Go Reflection Struct Inspection and Tags]]` и `[[Go Reflection Mutation and Dynamic Calls]]`.
4. Затем перейти к `[[Go Reflection Dynamic Decoding]]` как к прикладному кейсу.
5. Завершить `[[Go Reflection vs Generics vs Code Generation]]` и `[[Go Reflection Performance and Limits]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Go Type System]]`
- `[[Go Memory Management]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные статьи про `Go Type Assertions` и `Empty Interface and any in Go`
- [ ] Проверить, нужен ли отдельный article про `Reflection Safety Patterns in Go`
- [ ] Проверить `related`
