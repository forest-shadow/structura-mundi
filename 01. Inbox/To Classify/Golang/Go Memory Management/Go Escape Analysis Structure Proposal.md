---
aliases:
  - Golang Escape Analysis Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Memory Management]]"
status: draft
related:
  - "[[Go Escape Analysis]]"
  - "[[Go Memory Management]]"
  - "[[Go Toolchain]]"
  - "[[Go]]"
tags: []
---

# Go Escape Analysis Structure Proposal

## Краткое определение

Предлагаемое место для `Go Escape Analysis` внутри ветки `Go Memory Management` как отдельной article-note про компиляторное решение о размещении значений на стеке или в куче.

## Рекомендуемая иерархия

```text
Go
└── Go Memory Management
    ├── Go Stack and Heap Allocation
    ├── Go Escape Analysis
    └── Go Garbage Collection
```

## Почему структура именно такая

- `Go Escape Analysis` достаточно важен как самостоятельная статья, потому что он связывает поведение компилятора с реальными performance-последствиями.
- Теперь отдельный `overview` `Go Memory Management` уже оправдан, потому что рядом есть не только escape analysis, но и устойчивые соседние memory-related topics.
- Поэтому логичнее держать `Go Escape Analysis` дочерним article-узлом под `[[Go Memory Management]]`, а не прямым child-узлом верхнего уровня `Go`.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельный специализированный template под compiler/runtime notes.
- Не стоит делать каноническую заметку с общим именем `Escape Analysis`, если пока рассматривается именно Go-специфический контекст.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── G/
    ├── Go Memory Management.md
    ├── Go Stack and Heap Allocation.md
    ├── Go Escape Analysis.md
    └── Go Garbage Collection.md
```

## Что уже создано в Inbox

- `[[Go Memory Management]]`
- `[[Go Escape Analysis]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, нужны ли рядом `Go Inlining` или `Go SSA`
- [ ] Уточнить границы между memory management и memory model
- [ ] Проверить `related`
