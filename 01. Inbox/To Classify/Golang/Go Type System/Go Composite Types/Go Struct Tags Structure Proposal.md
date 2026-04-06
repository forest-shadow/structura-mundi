---
aliases:
  - Go Struct Tags Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: draft
related:
  - "[[Go Composite Types]]"
  - "[[Go Struct Types]]"
  - "[[Go Struct Tags]]"
  - "[[Go Reflection Struct Inspection and Tags]]"
tags: []
---

# Go Struct Tags Structure Proposal

## Предлагаемое положение в иерархии

```text
Go
└── Go Type System
    └── Go Composite Types
        ├── Go Struct Types
        └── Go Struct Tags
```

## Почему именно так

`Go Struct Tags` лучше размещать рядом с `[[Go Struct Types]]`, потому что теги являются частью описания полей структуры на уровне языка. Это не отдельная product-like ветка и не частный subsection внутри `[[Go Reflection]]`.

Reflection здесь остаётся соседней перспективой: он объясняет, как теги читаются и используются во время выполнения, но не задаёт их место в онтологии языка.

## Что должно входить в заметку

- синтаксис тегов в объявлении `struct`;
- семантическая роль тегов как метаданных;
- различие между языковым механизмом и библиотечными соглашениями;
- связь с reflection как механизмом чтения тегов.

## Что пока не нужно создавать

- отдельный overview вроде `Go Struct Metadata`;
- отдельные заметки под каждую конвенцию `json`, `yaml`, `db`, `validate`;
- специальные template-файлы под эту тему.

## Какие заметки нужны в ветке

- [[Go Struct Tags]]
- [[Go Struct Types]]
- [[Go Reflection Struct Inspection and Tags]]

## Практический маршрут чтения

`[[Go Type Literals]]` -> `[[Go Composite Types]]` -> `[[Go Struct Types]]` -> `[[Go Struct Tags]]` -> `[[Go Reflection Struct Inspection and Tags]]`