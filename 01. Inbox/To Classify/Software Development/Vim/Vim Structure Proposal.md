---
aliases:
  - Vim Branch Structure Proposal
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Software Development]]"
status: draft
related:
  - "[[Vim]]"
  - "[[Software Development]]"
  - "[[Vim Modes]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
tags: []
---

# Vim Structure Proposal

## Краткое определение

Предлагаемая иерархия заметок для ветки `Vim` внутри `Software Development`.

## Рекомендуемая иерархия

```text
Software Development
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

- `Vim` оправдан как отдельный overview, потому что тема уже естественно распадается на несколько устойчивых article-слоев.
- `Vim Modes` лучше держать отдельно, потому что modal model — это базовая рамка для чтения всей ветки.
- `Vim Motions`, `Vim Operators` и `Vim Text Objects` образуют ядро editing language, но пока разумнее держать их sibling-статьями без дополнительного sub-overview.
- `Vim Registers` и `Vim Macros` стоит выделить отдельно, потому что они отвечают за повторное использование текста и действий, а не просто за navigation.
- `Vim Buffers, Windows, and Tabs` лучше сначала держать одной заметкой, чтобы не раздувать ветку раньше времени.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельные notes под каждую отдельную команду, объект или shortcut.
- Не стоит раньше времени заводить отдельный sub-overview про `Editing Language`, если текущая ветка и так остается читаемой.
- Не стоит создавать специальные template-файлы под `Vim`: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный узел про command-line mode и ex-commands
- [ ] Проверить, когда buffers, windows и tabs лучше разнести по отдельным notes
- [ ] Проверить `related`
