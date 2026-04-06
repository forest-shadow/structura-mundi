---
aliases:
  - Vim Command System Structure Proposal
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Vim]]"
status: draft
related:
  - "[[Vim]]"
  - "[[Vim Commands]]"
  - "[[Vim Modes]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
  - "[[Vim Ex Commands]]"
tags: []
---

# Vim Commands Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Vim Commands` внутри более общей ветки `Vim` по правилам `Principia Rerum`.

## Рекомендуемая иерархия

```text
Vim
├── Vim Modes
│   └── Vim Command-line Mode
└── Vim Commands
    ├── Vim Motions
    ├── Vim Operators
    ├── Vim Text Objects
    └── Vim Ex Commands
```

## Почему структура именно такая

- `Vim Commands` лучше делать дочерним `overview`, а не обычной article-note, потому что тема уже естественно собирает несколько устойчивых семейств команд.
- `Vim Motions`, `Vim Operators` и `Vim Text Objects` образуют ядро command language Vim и поэтому лучше читаются как дочерние статьи одной рамки, а не как случайный набор sibling-заметок.
- `Vim Command-line Mode` не стоит подчинять `Vim Commands`, потому что это прежде всего mode-level понятие. Оно связано с командной веткой через `related`, но логически живет внутри `[[Vim Modes]]`.
- `Vim Ex Commands` стоит держать прямо под `Vim Commands`, потому что это уже не режим, а семейство команд, вводимых через `:`.

## Что не стоит создавать прямо сейчас

- Не стоит делать отдельные заметки под каждую конкретную команду вроде `:w`, `:q`, `d`, `c`, `y` или `ciw`.
- Не стоит раньше времени вводить еще один overview вроде `Vim Editing Language`, если `Vim Commands` уже покрывает этот кластер.
- Не стоит делать специальные template-файлы под `Vim Commands`: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`, а предметная специфика должна жить в самих заметках.

## Что стоит раскрыть дальше

- [ ] Проверить, когда внутри `Vim Ex Commands` нужен отдельный sub-overview про search, substitute и range-based editing
- [ ] Проверить, не требует ли `Vim Command-line Mode` отдельной связки с search- и filter-командами
- [ ] Проверить `related`
