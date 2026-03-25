---
aliases:
  - Type System in Go
  - Система типов Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go]]"
  - "[[Go Interfaces]]"
  - "[[Go Methods and Method Sets]]"
  - "[[Go Assignability and Conversions]]"
tags: []
---

# Go Type System

## Краткое определение области

Обзорная заметка про систему типов Go: какие типовые категории в ней есть, как в ней устроены identity и compatibility, каким образом методы и интерфейсы выражают поведение и где в эту картину входят type parameters.

## Что входит в эту тему

- `[[Go Basic Types]]`
- `[[Go Composite Types]]`
- `[[Go Defined Types and Underlying Types]]`
- `[[Go Assignability and Conversions]]`
- `[[Go Methods and Method Sets]]`
- `[[Go Interfaces]]`
- `[[Go Type Parameters and Constraints]]`

## Как устроена ветка

- `Go Basic Types` и `Go Composite Types` фиксируют канонические семейства типов, с которыми язык работает как с формами данных.
- `Go Defined Types and Underlying Types` объясняет, как в Go соотносятся именование типа, его identity и underlying representation.
- `Go Assignability and Conversions` собирает правила, по которым значения могут переходить между типами или требовать явного преобразования.
- `Go Methods and Method Sets` раскрывает поведенческий слой типовой системы и подводит почву к интерфейсам.
- `Go Interfaces` выделены в отдельную article-note как особый вид типов и механизм структурной абстракции.
- `Go Type Parameters and Constraints` добавляет слой parametric polymorphism, но не отменяет базовые правила identity, assignability и method sets.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Basic Types]]` и `[[Go Composite Types]]`, чтобы зафиксировать сами семейства типов.
2. Затем перейти к `[[Go Defined Types and Underlying Types]]`, чтобы понять identity и именование типов.
3. После этого читать `[[Go Assignability and Conversions]]`, где видно, как типы соотносятся в программах.
4. Затем перейти к `[[Go Methods and Method Sets]]` как к мосту между типами и поведением.
5. После этого читать `[[Go Interfaces]]`, потому что именно там structural typing начинает работать как практический механизм.
6. Завершить `[[Go Type Parameters and Constraints]]`, когда уже понятны базовые типы, совместимость и method sets.

## Соседние ветки

- `[[Go Error Handling]]`
- `[[Go Memory Management]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Go Zero Value and Nil`
- [ ] Решить, стоит ли выделять `Go Type Assertions`
- [ ] Уточнить границы между `Go Composite Types` и более узкими notes вроде `slice` или `map`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
