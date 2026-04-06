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
  - "[[Vim Commands]]"
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
    │   └── Vim Command-line Mode
    ├── Vim Commands
    │   ├── Vim Motions
    │   ├── Vim Operators
    │   ├── Vim Text Objects
    │   └── Vim Ex Commands
    ├── Vim Registers
    ├── Vim Macros
    └── Vim Buffers, Windows, and Tabs
```

## Почему структура именно такая

- `Vim` оправдан как отдельный overview, потому что тема уже естественно распадается на несколько устойчивых article-слоев.
- `Vim Modes` лучше держать отдельно, потому что modal model — это базовая рамка для чтения всей ветки.
- `Vim Commands` уже оправдан как локальный `sub-overview`, потому что `Vim Motions`, `Vim Operators` и `Vim Text Objects` образуют не просто набор соседних статей, а устойчивый кластер про командную грамматику редактора.
- `Vim Command-line Mode` лучше держать под `Vim Modes`, а не под `Vim Commands`, потому что это прежде всего состояние редактора, через которое уже вводятся `Ex`-команды, search-выражения и filter-команды.
- `Vim Ex Commands` естественно входят в `Vim Commands`, потому что это уже отдельное семейство команд, а не просто частный пример внутри `Vim Command-line Mode`.
- `Vim Registers` и `Vim Macros` стоит выделить отдельно, потому что они отвечают за повторное использование текста и действий, а не просто за navigation.
- `Vim Buffers, Windows, and Tabs` лучше сначала держать одной заметкой, чтобы не раздувать ветку раньше времени.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельные notes под каждую отдельную команду, объект или shortcut.
- Не стоит заводить еще один промежуточный overview между `Vim` и `Vim Commands`, потому что это только усложнит ветку без дополнительного смысла.
- Не стоит создавать специальные template-файлы под `Vim`: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда внутри `Vim Commands` появляются отдельные article-заметки про ranges, search/replace и global-команды
- [ ] Проверить, когда buffers, windows и tabs лучше разнести по отдельным notes
- [ ] Проверить `related`
