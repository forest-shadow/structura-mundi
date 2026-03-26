---
aliases:
  - Go Reflection Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: draft
related:
  - "[[Go Reflection]]"
  - "[[Go Type System]]"
  - "[[reflect.Type, reflect.Value and reflect.Kind]]"
  - "[[Addressability and Settable Values in Go Reflection]]"
tags: []
---

# Go Reflection Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Go Reflection` по правилам `Principia Rerum`.

Ветка размещается внутри уже существующей Go-ветки и не требует нового `section`:

- `area: computer-science`
- `domain: programming-languages`
- `section: go`

Здесь нет необходимости вводить отдельный `section`, потому что reflection остается локальным подкластером внутри устойчивой языковой ветки `Go`, а не отдельным крупным доменом.

## Рекомендуемая иерархия

```text
Go
└── Go Type System
    └── Go Reflection
        ├── reflect.Type, reflect.Value and reflect.Kind
        ├── Addressability and Settable Values in Go Reflection
        ├── Struct Inspection and Tags in Go Reflection
        ├── Dynamic Operations in Go Reflection
        ├── Reflection and Dynamic Decoding in Go
        ├── Reflection vs Generics vs Code Generation in Go
        └── Performance and Limits of Go Reflection
```

## Почему структура именно такая

- `Go Reflection` уже оправдана как `sub-overview`, потому что тема не сводится к одной explanatory article: внутри нее есть отдельный понятийный фундамент, слой ограничений, прикладные сценарии и архитектурные сравнения.
- `reflect.Type, reflect.Value and reflect.Kind` должна быть первой частной статьей, потому что без нее остальные заметки будут ссылаться на термины reflection без устойчивого общего основания.
- `Addressability and Settable Values in Go Reflection` нужно выделять отдельно, потому что именно здесь находятся ключевые runtime-ограничения reflection и большинство практических ошибок.
- `Struct Inspection and Tags in Go Reflection` образует устойчивый прикладной кластер, поскольку в реальном Go reflection очень часто используется для анализа структур и тегов.
- `Dynamic Operations in Go Reflection` собирает тот слой API, где reflection уже не только читает, но и создает, меняет и вызывает значения, поэтому его полезно держать отдельно от базовой инспекции.
- `Reflection and Dynamic Decoding in Go` лучше выносить как отдельный кейс, потому что это уже инженерная задача, а не только перечень API-приемов.
- `Reflection vs Generics vs Code Generation in Go` и `Performance and Limits of Go Reflection` являются завершающими аналитическими заметками, а не продолжением базового API-описания.

## Что пока не нужно создавать

- `Mutation Through Go Reflection` и `Dynamic Method Calls in Go Reflection` как две отдельные статьи, пока для старта достаточно объединенного узла `Dynamic Operations in Go Reflection`
- отдельные note-файлы про каждый метод `reflect.Value`, пока важнее удержать смысловые кластеры
- специальный template-файл под reflection-ветку, потому что по `Principia Rerum` достаточно канонических `overview/article`

## Созданные черновые заметки

- `Go Reflection.md`
- `reflect.Type, reflect.Value and reflect.Kind.md`
- `Addressability and Settable Values in Go Reflection.md`
- `Struct Inspection and Tags in Go Reflection.md`
- `Dynamic Operations in Go Reflection.md`
- `Reflection and Dynamic Decoding in Go.md`
- `Reflection vs Generics vs Code Generation in Go.md`
- `Performance and Limits of Go Reflection.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границы между `Go Reflection`, `Go Interfaces` и возможной будущей заметкой про `Go Type Assertions`.
2. Решить, нужен ли позднее отдельный article про `any`, interface values и runtime type assertions рядом с reflection-веткой.
3. После этого перевести seed-заметки в содержательные черновики и нормализовать `related`.
