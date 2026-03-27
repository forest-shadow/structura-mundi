---
aliases:
  - Go Basic Types Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: draft
related:
  - "[[Go Basic Types]]"
  - "[[Go Type System]]"
  - "[[Go Integer Types]]"
tags: []
---

# Go Basic Types Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Go Basic Types` по правилам `Principia Rerum`.

Ветка размещается внутри `Go Type System` и не требует нового `section`:

- `area: computer-science`
- `domain: programming-languages`
- `section: go`

## Рекомендуемая иерархия

```text
Go
└── Go Type System
    └── Go Basic Types
        ├── Go Boolean Type
        ├── Go String Type
        ├── Go Integer Types
        ├── Go Floating-Point Types
        └── Go Complex Types
```

## Почему структура именно такая

- `Go Basic Types` уже оправдан как `sub-overview`, потому что тема делится не на случайные builtin names, а на устойчивые семейства типов.
- `Go Boolean Type` и `Go String Type` остаются отдельными статьями, потому что это самостоятельные basic types с собственной семантикой, но без нужды в дополнительной локальной иерархии.
- `Go Integer Types` заслуживает отдельной статьи, потому что именно здесь сходятся signed и unsigned integers, platform-dependent типы `int` и `uint`, fixed-width типы и alias-имена `byte` и `rune`.
- `Go Floating-Point Types` и `Go Complex Types` лучше держать отдельными заметками, потому что это естественные numeric families с собственными операциями и ограничениями.

## Что пока не нужно создавать

- отдельные notes для каждого builtin вроде `int8`, `uint32`, `float64` или `complex128`, пока достаточно семейств типов;
- отдельную note только про `byte` или только про `rune`, пока они естественно раскрываются внутри `Go Integer Types`;
- специальный template-файл под basic-types ветку, потому что по `Principia Rerum` достаточно канонических `overview/article` шаблонов.

## Созданные черновые заметки

- `Go Basic Types.md`
- `Go Boolean Type.md`
- `Go String Type.md`
- `Go Integer Types.md`
- `Go Floating-Point Types.md`
- `Go Complex Types.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границы между `Go Integer Types` и возможной будущей заметкой про untyped constants.
2. Проверить, когда `Go String Type` стоит связывать с отдельной заметкой про runes, UTF-8 и text processing.
3. После этого перевести seed-заметки в содержательные черновики и нормализовать `related`.
