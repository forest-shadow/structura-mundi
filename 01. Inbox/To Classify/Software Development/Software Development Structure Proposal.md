---
aliases:
  - Software Development Domain Structure Proposal
note_type: article
area: computer-science
domain: software-development
section:
parent: "[[Computer Science]]"
status: draft
related:
  - "[[Software Development]]"
  - "[[Computer Science]]"
  - "[[Vim]]"
  - "[[Programming Languages]]"
  - "[[Software Architecture]]"
tags: []
---

# Software Development Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию для новой доменной ветки `Software Development` внутри `Computer Science` по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: software-development`
- `section:` пусто у domain-root overview `Software Development`

Почему так:

- ветка собирает не одну заметку, а потенциально устойчивый корпус про редакторы, version control, build tooling, test tooling и рабочие инструменты разработчика;
- существующие `domain` вроде `programming-languages` и `software-architecture` не покрывают этот слой без смыслового искажения;
- корневая заметка `Software Development` описывает весь домен, поэтому не должна получать служебный `section`.

## Рекомендуемая иерархия

```text
Computer Science
└── Software Development
    └── Vim
        ├── Vim Modes
        ├── Vim Motions
        ├── Vim Operators
        ├── Vim Text Objects
        ├── Vim Registers
        ├── Vim Macros
        └── Vim Buffers, Windows, and Tabs
```

## Почему структура именно такая

- `Software Development` нужен как domain-root, чтобы заметки про инструменты разработки не висели напрямую под `Computer Science` и не подмешивались к языкам или архитектуре.
- `Vim` оправдан как section-level overview, потому что это не одна isolated article, а плотный кластер вокруг modal editing, editing language и рабочей модели редактора.
- Дополнительный sub-overview внутри `Vim` пока не нужен: ветка естественно собирается плоским набором article-заметок.

## Что не стоит создавать заранее

- отдельный overview `Modal Editing`, если пока вся плотность корпуса сосредоточена внутри `Vim`;
- отдельные notes по каждой отдельной команде вроде `dw` или `ciw`;
- отдельные template-файлы под developer tooling, потому что по `Principia Rerum` должны оставаться только канонические `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `Vim` нужны `Git` и build-tooling ветки
- [ ] Проверить, нужен ли позже более общий section-level узел для editor tooling
- [ ] Проверить `related`
