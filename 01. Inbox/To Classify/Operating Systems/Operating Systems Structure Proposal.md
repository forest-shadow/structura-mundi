---
aliases:
  - OS Structure Proposal
note_type: article
area: computer-science
domain: operating-systems
section:
parent:
status: draft
related:
  - "[[Operating Systems]]"
  - "[[Processes and Threads]]"
  - "[[Virtual Memory]]"
  - "[[System Calls]]"
  - "[[File Systems]]"
  - "[[Containerization]]"
  - "[[Linux]]"
tags: []
---

# Operating Systems Structure Proposal

## Краткое определение

Рабочая seed-иерархия `Operating Systems` в `Inbox`, без переноса в `Corpus Mundi`.

## Рекомендуемая иерархия

```text
Operating Systems [overview]
├── Processes and Threads [overview]
│   ├── Process [overview]
│   │   └── Process State Model [article]
│   ├── Thread [article]
│   ├── CPU Scheduling [overview]
│   │   └── Context Switch [article]
│   ├── Interprocess Communication [article]
│   └── Synchronization Primitives [overview]
│       ├── Race Condition [article]
│       └── Data Race [article]
├── System Calls [article]
├── File Systems [article]
├── Virtual Memory [overview]
│   ├── Virtual Address Space [article]
│   └── Paging [overview]
│       ├── Page Table [article]
│       ├── TLB [article]
│       └── Page Fault [article]
├── Linux [overview]
│   ├── Linux Kernel [article]
│   ├── Linux Distribution [article]
│   └── Linux File System [overview]
│       ├── Filesystem Hierarchy Standard [article]
│       └── Linking Files [overview]
│           ├── Hard Link [article]
│           └── Symbolic Link [article]
└── Containerization [overview]
    └── Docker [article]
```

## Почему структура именно такая

- `Operating Systems` остаётся domain-root overview.
- `Processes and Threads`, `Virtual Memory`, `Linux` и `Containerization` оформлены как overview-ветки, потому что у них уже есть устойчивые дочерние кластеры.
- `System Calls` и `File Systems` пока достаточно держать как обычные articles.
- Ветка существует как seed-корпус в `Inbox`; публикация в `Corpus Mundi` здесь не предполагается.

## Что уже зафиксировано

- `Process` поднят до `overview`, чтобы `Process State Model` был корректным дочерним article.
- `CPU Scheduling` поднят до `overview`, чтобы `Context Switch` был корректным дочерним article.
- `Linux` и `Containerization` зафиксированы как sibling-ветки под `Operating Systems`.
