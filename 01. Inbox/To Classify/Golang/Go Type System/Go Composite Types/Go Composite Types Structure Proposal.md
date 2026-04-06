---
aliases:
  - Go Composite Types Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: draft
related:
  - "[[Go Type System]]"
  - "[[Go Type Literals]]"
  - "[[Go Composite Types]]"
tags: []
---

# Go Composite Types Structure Proposal

## Что это за узел

`[[Go Composite Types]]` - это обзорная точка для составных типов Go, то есть для тех типовых форм, где значение определяется не одним базовым атомом, а структурой, комбинацией или отношением между элементами.

## Предлагаемая иерархия внутри ветки

```text
Go Composite Types
├── Go Array Types
├── Go Slice Types
├── Go Map Types
├── Go Struct Types
├── Go Struct Tags
├── Go Pointer Types
├── Go Function Types
├── Go Interface Types
└── Go Channel Types
```

## Почему `Go Struct Tags` находятся здесь

`[[Go Struct Tags]]` не стоит прятать только в `[[Go Reflection]]`, потому что теги принадлежат синтаксису и устройству полей `struct` на уровне языка. Reflection лишь даёт доступ к этим данным во время выполнения.

При этом создавать отдельный overview-узел вроде `Go Struct Metadata` пока не нужно: для текущего масштаба темы достаточно одной самостоятельной заметки рядом с `[[Go Struct Types]]`.

## Какой маршрут чтения получается

`[[Go Type Literals]]` -> `[[Go Composite Types]]` -> `[[Go Struct Types]]` -> `[[Go Struct Tags]]`

Оттуда уже естественно переходить в `[[Go Reflection Struct Inspection and Tags]]`, если нужно рассмотреть runtime-доступ к полям и тегам.

## Что пока не нужно выносить в отдельные заметки

- теги стандартных пакетов по отдельности;
- library-specific соглашения под каждую экосистему;
- шаблонные файлы для каждой подтемы ветки.

## Какие заметки уже оправданы

- [[Go Array Types]]
- [[Go Slice Types]]
- [[Go Map Types]]
- [[Go Struct Types]]
- [[Go Struct Tags]]
- [[Go Pointer Types]]
- [[Go Function Types]]
- [[Go Interface Types]]
- [[Go Channel Types]]