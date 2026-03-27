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
  - "[[Go Reflection Type and Value Model]]"
  - "[[Go Reflection Addressability and Settable Values]]"
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
        ├── Go Reflection Type and Value Model
        ├── Go Reflection Addressability and Settable Values
        ├── Go Reflection Struct Inspection and Tags
        ├── Go Reflection Mutation and Dynamic Calls
        ├── Go Reflection Dynamic Decoding
        ├── Go Reflection vs Generics vs Code Generation
        └── Go Reflection Performance and Limits
```

## Почему структура именно такая

- `Go Reflection` уже оправдана как `sub-overview`, потому что тема не сводится к одной explanatory article: внутри нее есть отдельный понятийный фундамент, слой ограничений, прикладные сценарии и архитектурные сравнения.
- `Go Reflection Type and Value Model` должна быть первой частной статьей, потому что без нее остальные заметки будут ссылаться на термины reflection без устойчивого общего основания.
- `Go Reflection Addressability and Settable Values` нужно выделять отдельно, потому что именно здесь находятся ключевые runtime-ограничения reflection и большинство практических ошибок.
- `Go Reflection Struct Inspection and Tags` образует устойчивый прикладной кластер, поскольку в реальном Go reflection очень часто используется для анализа структур и тегов.
- `Go Reflection Mutation and Dynamic Calls` собирает тот слой API, где reflection уже не только читает, но и создает, меняет и вызывает значения, поэтому его полезно держать отдельно от базовой инспекции.
- `Go Reflection Dynamic Decoding` лучше выносить как отдельный кейс, потому что это уже инженерная задача, а не только перечень API-приемов.
- `Go Reflection vs Generics vs Code Generation` и `Go Reflection Performance and Limits` являются завершающими аналитическими заметками, а не продолжением базового API-описания.

## Что пока не нужно создавать

- `Mutation Through Go Reflection` и `Dynamic Method Calls in Go Reflection` как две отдельные статьи, пока для старта достаточно объединенного узла `Go Reflection Mutation and Dynamic Calls`
- отдельные note-файлы про каждый метод `reflect.Value`, пока важнее удержать смысловые кластеры
- специальный template-файл под reflection-ветку, потому что по `Principia Rerum` достаточно канонических `overview/article`

## Созданные черновые заметки

- `Go Reflection.md`
- `Go Reflection Type and Value Model.md`
- `Go Reflection Addressability and Settable Values.md`
- `Go Reflection Struct Inspection and Tags.md`
- `Go Reflection Mutation and Dynamic Calls.md`
- `Go Reflection Dynamic Decoding.md`
- `Go Reflection vs Generics vs Code Generation.md`
- `Go Reflection Performance and Limits.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границы между `Go Reflection`, `Go Interfaces` и возможной будущей заметкой про `Go Type Assertions`.
2. Решить, нужен ли позднее отдельный article про `any`, interface values и runtime type assertions рядом с reflection-веткой.
3. После этого перевести seed-заметки в содержательные черновики и нормализовать `related`.
