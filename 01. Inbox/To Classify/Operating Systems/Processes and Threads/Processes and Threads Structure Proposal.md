---
aliases:
  - Processes and Threads Structure Proposal
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Processes and Threads]]"
status: draft
related:
  - "[[Processes and Threads]]"
  - "[[Operating Systems]]"
  - "[[Synchronization Primitives]]"
  - "[[Race Condition]]"
  - "[[Data Race]]"
tags: []
---

# Processes and Threads Structure Proposal

## Краткое определение

Рабочая seed-иерархия ветки `Processes and Threads` внутри `Operating Systems`.

## Рекомендуемая иерархия

```text
Operating Systems [overview]
└── Processes and Threads [overview]
    ├── Process [overview]
    │   └── Process State Model [article]
    ├── Thread [article]
    ├── CPU Scheduling [overview]
    │   └── Context Switch [article]
    ├── Interprocess Communication [article]
    └── Synchronization Primitives [overview]
        ├── Race Condition [article]
        └── Data Race [article]
```

## Почему структура именно такая

- `Processes and Threads` остаётся локальным overview-узлом execution model.
- `Process` и `CPU Scheduling` оформлены как overview-узлы, потому что у них есть дочерние articles.
- `Thread` и `Interprocess Communication` пока остаются обычными articles.
- `Synchronization Primitives` оформлен как overview, потому что уже собирает дочерние failure-mode notes.
