---
aliases:
  - Go Composite Types Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: draft
related:
  - "[[Go Composite Types]]"
  - "[[Go Type System]]"
  - "[[Go Type Literals]]"
  - "[[Go Interfaces]]"
tags: []
---

# Go Composite Types Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Go Composite Types` по правилам `Principia Rerum`.

Ветка размещается внутри `Go Type System` и не требует нового `section`:

- `area: computer-science`
- `domain: programming-languages`
- `section: go`

## Рекомендуемая иерархия

```text
Go
└── Go Type System
    └── Go Composite Types
        ├── Go Type Literals
        ├── Go Array Types
        ├── Go Struct Types
        ├── Go Pointer Types
        ├── Go Function Types
        ├── Go Interfaces
        ├── Go Slice Types
        ├── Go Map Types
        └── Go Channel Types
```

## Почему структура именно такая

- `Go Composite Types` уже оправдан как `sub-overview`, потому что тема распадается не на случайный список builtin forms, а на устойчивые type-literal families.
- `Go Type Literals` нужна как первая частная статья, потому что без нее composite branch будет перечислять формы типов без общего объяснения принципа.
- `Go Array Types` и `Go Struct Types` логично держать рядом как фиксированные составные формы, где shape значения входит в тип.
- `Go Pointer Types` и `Go Function Types` стоит выделять отдельно, потому что это самостоятельные composite forms, не сводимые ни к контейнерам, ни к record-like структурам.
- `Go Interfaces` не нужно дублировать отдельной note вроде `Go Interface Type`: существующая каноническая заметка уже покрывает interface form и должна просто жить внутри composite branch.
- `Go Slice Types`, `Go Map Types` и `Go Channel Types` образуют cluster динамических runtime-backed composite forms.

## Что пока не нужно создавать

- отдельные notes про каждый частный literal pattern вроде `chan<- T` или `[N]T`, пока достаточно семейства типов;
- отдельную дублирующую note `Go Interface Type`, потому что канонический узел уже есть в виде `Go Interfaces`;
- специальный template-файл под composite-types ветку, потому что по `Principia Rerum` достаточно канонических `overview/article` шаблонов.

## Созданные черновые заметки

- `Go Composite Types.md`
- `Go Type Literals.md`
- `Go Array Types.md`
- `Go Struct Types.md`
- `Go Pointer Types.md`
- `Go Function Types.md`
- `Go Interfaces.md`
- `Go Slice Types.md`
- `Go Map Types.md`
- `Go Channel Types.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить, когда `Go Interfaces` стоит сильнее развести на ordinary interfaces и constraints.
2. Проверить, когда `Go Slice Types` и `Go Map Types` потребуют более глубоких дочерних веток.
3. После этого перевести seed-заметки в содержательные черновики и нормализовать `related`.
