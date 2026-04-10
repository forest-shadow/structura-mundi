---
aliases:
  - Go Knowledge Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Programming Languages]]"
status: draft
related:
  - "[[Go]]"
  - "[[Programming Languages]]"
  - "[[Software Engineering]]"
tags: []
---

# Go Structure Proposal

## Что это за узел

`[[Go]]` должен быть обзорной точкой для языка Go как целостной темы: синтаксис, типовая система, memory model, concurrency, tooling, ecosystem и idiomatic style.

## Предлагаемая общая иерархия

```text
Programming Languages
└── Go
    ├── Go Syntax and Lexical Structure
    ├── Go Type System
    │   ├── Go Basic Types
    │   ├── Go Composite Types
    │   │   ├── Go Array Types
    │   │   ├── Go Slice Types
    │   │   ├── Go Map Types
    │   │   ├── Go Struct Types
    │   │   ├── Go Struct Tags
    │   │   ├── Go Pointer Types
    │   │   ├── Go Function Types
    │   │   ├── Go Interface Types
    │   │   └── Go Channel Types
    │   ├── Go Type Literals
    │   ├── Go Type Identity
    │   ├── Go Type Definitions
    │   ├── Go Type Constraints
    │   └── Go Reflection
    ├── Go Control Flow
    ├── Go Functions and Methods
    ├── Go Packages and Modules
    ├── Go Error Handling
    ├── Go Concurrency
    ├── Go Memory Model
    ├── Go Runtime Diagnostics
    │   └── Go pprof
    │       ├── Go pprof Profile Types
    │       ├── Go pprof Collection Methods
    │       └── Go pprof Analysis Workflow
    ├── Go Standard Library
    ├── Go Tooling
    └── Go Idioms
```

## Почему структура такая

Ветка должна сначала показывать Go как язык, а затем расходиться по устойчивым conceptual layers: форма исходного кода, устройство типов, исполнение, concurrency и tooling. Это помогает не смешивать language semantics с библиотечными практиками или инструментами.

`[[Go Struct Tags]]` имеет смысл держать в `[[Go Type System]]` рядом с `[[Go Struct Types]]`, потому что struct tags принадлежат объявлению поля на уровне языка. Их runtime-чтение через reflection уже является вторичной перспективой, а не исходной категорией.

`[[Go Runtime Diagnostics]]` имеет смысл держать отдельным overview-узлом рядом с `[[Go Memory Management]]` и `[[Go Concurrency Model]]`, потому что profiling, tracing и runtime-analysis практики используют эти темы, но не сводятся ни к одной из них. `[[Go pprof]]` помещается внутрь этой ветки как первый устойчивый диагностический инструмент.

## Что стоит включать в языковой слой

- [[Go Syntax and Lexical Structure]]
- [[Go Type System]]
- [[Go Basic Types]]
- [[Go Composite Types]]
- [[Go Struct Types]]
- [[Go Struct Tags]]
- [[Go Reflection]]
- [[Go Control Flow]]
- [[Go Functions and Methods]]
- [[Go Packages and Modules]]
- [[Go Error Handling]]
- [[Go Concurrency]]
- [[Go Memory Model]]
- [[Go Runtime Diagnostics]]
- [[Go pprof]]

## Что не стоит делать

- не превращать верхний уровень в список всех пакетов стандартной библиотеки;
- не выносить library conventions в язык без оговорок;
- не создавать промежуточные overview-узлы без достаточного количества самостоятельных подтем.
- не создавать отдельный `section: pprof`, потому что `section: go` уже задаёт нужный локальный кластер.

## Практический маршрут чтения

`[[Go]]` -> `[[Go Type System]]` -> `[[Go Composite Types]]` -> `[[Go Struct Types]]` -> `[[Go Struct Tags]]` -> `[[Go Reflection Struct Inspection and Tags]]`
