---
aliases:
  - Golang Escape Analysis Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go Escape Analysis]]"
  - "[[Go Toolchain]]"
  - "[[Go]]"
tags: []
---

# Go Escape Analysis Structure Proposal

## Краткое определение

Предлагаемое место для `Go Escape Analysis` внутри ветки `Go` как отдельной article-note про компиляторное решение о размещении значений на стеке или в куче.

## Рекомендуемая иерархия

```text
Go
├── Go Toolchain
├── Go Escape Analysis
├── Go Packages and Modules
├── Go Type System
├── Go Interfaces
├── Go Error Handling
├── Go Concurrency Model
│   ├── Go Goroutines
│   └── Go Channels
└── Go Testing
```

## Почему структура именно такая

- `Go Escape Analysis` достаточно важен как самостоятельная статья, потому что он связывает поведение компилятора с реальными performance-последствиями.
- При этом отдельный `overview` вроде `Go Compiler` или `Go Memory Behavior` пока избыточен: в текущей ветке еще нет плотного набора sibling-notes, который бы оправдывал новый промежуточный узел.
- Поэтому сейчас логичнее держать `Go Escape Analysis` прямым дочерним article-узлом под `[[Go]]`, а связь с компиляторной частью фиксировать через `related` и содержание.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельный специализированный template под compiler/runtime notes.
- Не стоит вводить новый sub-overview только ради одной заметки.
- Не стоит делать каноническую заметку с общим именем `Escape Analysis`, если пока рассматривается именно Go-специфический контекст.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── G/
    └── Go Escape Analysis.md
```

## Что уже создано в Inbox

- `[[Go Escape Analysis]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда в ветке Go появится достаточно compiler-related notes для отдельного overview
- [ ] Уточнить, нужны ли рядом `Go Inlining` или `Go SSA`
- [ ] Проверить `related`
