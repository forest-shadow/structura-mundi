---
aliases:
  - Go Type System Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go Type System]]"
  - "[[Go Basic Types]]"
  - "[[Go Composite Types]]"
  - "[[Go Type Literals]]"
  - "[[Go Type Identity]]"
  - "[[Go Type Definitions]]"
  - "[[Go Type Constraints]]"
  - "[[Go Reflection]]"
tags: []
---

# Go Type System Structure Proposal

## Что это за узел

`[[Go Type System]]` должен быть обзорной заметкой для всей ветки, описывающей, как в Go устроены типы, их формы, идентичность, совместимость, ограничения и связи с runtime.

## Предлагаемая иерархия

```text
Go
└── Go Type System
    ├── Go Basic Types
    ├── Go Composite Types
    │   ├── Go Array Types
    │   ├── Go Slice Types
    │   ├── Go Map Types
    │   ├── Go Struct Types
    │   ├── Go Struct Tags
    │   ├── Go Pointer Types
    │   ├── Go Function Types
    │   ├── Go Interface Types
    │   └── Go Channel Types
    ├── Go Type Literals
    ├── Go Type Identity
    ├── Go Type Definitions
    ├── Go Type Constraints
    └── Go Reflection
```

## Почему структура такая

Сначала ветка делится на формы типов, затем на правила и отношения между типами, и уже после этого - на runtime-perspective через reflection. Это позволяет не смешивать синтаксическую форму типа с поведением introspection API.

`[[Go Struct Tags]]` логично находятся внутри ветки composite types, потому что относятся к объявлению полей `struct` на уровне языка. Reflection остаётся рядом как механизм чтения этих тегов во время выполнения, но не как их основное онтологическое место.

## Что не стоит делать

- не стоит смешивать `Go Type System` с пакетом `reflect` как будто это одна тема;
- не стоит выносить каждую частную особенность синтаксиса в отдельный верхнеуровневый overview;
- не стоит дублировать одну и ту же тему и в type-system, и в runtime-ветке без чёткой границы.

## Практический маршрут чтения

`[[Go Type Literals]]` -> `[[Go Composite Types]]` -> `[[Go Struct Types]]` -> `[[Go Struct Tags]]` -> `[[Go Reflection]]` -> `[[Go Reflection Struct Inspection and Tags]]`

## Какие заметки уже особенно оправданы

- [[Go Basic Types]]
- [[Go Composite Types]]
- [[Go Type Literals]]
- [[Go Type Identity]]
- [[Go Type Definitions]]
- [[Go Type Constraints]]
- [[Go Reflection]]