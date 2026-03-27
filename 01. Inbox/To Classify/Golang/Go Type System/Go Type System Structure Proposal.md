---
aliases:
  - Golang Type System Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go Type System]]"
  - "[[Go Interfaces]]"
  - "[[Go]]"
tags: []
---

# Go Type System Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Go Type System` как отдельного `sub-overview` внутри `Go`, собирающего канонические категории типовой системы языка.

## Рекомендуемая иерархия

```text
Go
└── Go Type System
    ├── Go Basic Types
    ├── Go Composite Types
    ├── Go Defined Types and Underlying Types
    ├── Go Assignability and Conversions
    ├── Go Methods and Method Sets
    ├── Go Interfaces
    ├── Go Reflection
    │   ├── Go Reflection Type and Value Model
    │   ├── Go Reflection Addressability and Settable Values
    │   ├── Go Reflection Struct Inspection and Tags
    │   ├── Go Reflection Mutation and Dynamic Calls
    │   ├── Go Reflection Dynamic Decoding
    │   ├── Go Reflection vs Generics vs Code Generation
    │   └── Go Reflection Performance and Limits
    └── Go Type Parameters and Constraints
```

## Почему структура именно такая

- `Go Type System` уже не выглядит как одиночная explanatory article: внутри темы есть устойчивый набор канонических категорий, каждая из которых отвечает за отдельный слой типовой модели.
- `Go Basic Types` и `Go Composite Types` нужны как верхнеуровневое разделение между семействами типов.
- `Go Defined Types and Underlying Types` фиксирует одну из центральных идей Go: типовая идентичность не сводится к одной лишь форме представления.
- `Go Assignability and Conversions` нужен как отдельный узел, потому что совместимость типов и явные преобразования образуют самостоятельный класс правил.
- `Go Methods and Method Sets` стоит держать рядом с интерфейсами, поскольку именно через method sets в Go связываются типы и поведение.
- `Go Interfaces` остаются отдельной article-note, а не растворяются внутри method sets, потому что это самостоятельная canonical category системы типов и ключевая идиома языка.
- `Go Reflection` уже оправдан как отдельный `sub-overview`, потому что она собирает не один API-фрагмент, а целую локальную ветку про runtime type information, ограничения mutation и архитектурные trade-offs.
- `Go Type Parameters and Constraints` входят в современную типовую систему Go как слой parametric polymorphism и поэтому должны быть видны прямо в верхней структуре ветки.

## Что не стоит делать прямо сейчас

- Не стоит дробить ветку до отдельных notes про каждый built-in type, пока для этого нет устойчивого корпуса.
- Не стоит смешивать `Go Type System` с memory semantics или concurrency semantics.
- Не стоит делать reflection просто длинным хвостом внутри `Go Interfaces`: у нее уже есть собственный понятийный и прикладной кластер.
- Не стоит создавать специализированные templates под type-system notes.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Go Zero Value and Nil`
- [ ] Решить, когда стоит выделить `Go Type Assertions`
- [ ] Проверить, когда внутри `Go Reflection` нужны отдельные notes про `any` и interface values
- [ ] Проверить `related`
