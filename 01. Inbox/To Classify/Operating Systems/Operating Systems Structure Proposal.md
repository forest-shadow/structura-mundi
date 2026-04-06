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

Предлагаемая рабочая ветка `Operating Systems` собирает под одним корневым обзорным узлом базовые механизмы ОС: execution model, системные вызовы, файловые системы, memory-management ветку `Virtual Memory`, Linux-ветку `Linux` и containerization-ветку `Containerization`.

## Выбранная оптика

- `area: computer-science`
- `domain: operating-systems`
- `section:` пусто у domain-root overview `Operating Systems`

Почему так:

- тема не укладывается естественно в уже существующие соседние `domain`;
- для ОС нужен собственный предметный фокус, а не искусственное размещение в `software-architecture`;
- корневая заметка `Operating Systems` описывает весь `domain`, поэтому не должна получать служебный `section`;
- дочерние кластеры получают собственные локальные секции: `processes-and-threads`, `system-calls`, `file-systems`, `memory-management`, `linux` и `containerization`.

## Каноническое имя

- корневая обзорная заметка: `Operating Systems`
- `OS` и `Operating System` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Operating Systems
├── Processes and Threads
│   ├── Process
│   │   └── Process State Model
│   ├── Thread
│   ├── CPU Scheduling
│   │   └── Context Switch
│   ├── Interprocess Communication
│   └── Synchronization Primitives
│       ├── Race Condition
│       └── Data Race
├── System Calls
├── File Systems
├── Virtual Memory
│   ├── Virtual Address Space
│   └── Paging
│       ├── Page Table
│       ├── TLB
│       └── Page Fault
├── Linux
│   ├── Linux Kernel
│   ├── Linux Distribution
│   └── Linux File System
└── Containerization
    └── Docker
```

## Почему структура именно такая

- `Operating Systems` нужен как root `overview`, потому что рядом уже есть несколько самостоятельных смысловых кластеров, а не одна isolated article.
- `Processes and Threads` и `Virtual Memory` оправданы как `sub-overview`, потому что внутри них уже есть плотные дочерние подветки.
- `System Calls` и `File Systems` пока разумнее держать как обычные `article`, чтобы не усложнять ветку раньше времени.
- `Linux` уже оправдан как отдельный `sub-overview`, потому что тема естественно собирает не только ядро и дистрибутивы, но и Linux-specific механизмы вроде `Linux File System`.
- `Containerization` оправдана как отдельный `sub-overview`, потому что она собирает не один термин, а устойчивую группу тем о контейнерах, изоляции процессов, образах и runtime-модели.
- `Docker` естественно живёт внутри `Containerization`, а не напрямую под корнем `Operating Systems`, потому что это один конкретный инструментальный узел внутри более широкой темы.

## Текущая физическая раскладка в Inbox

```text
Operating Systems/
├── Operating Systems.md
├── Operating Systems Structure Proposal.md
├── System Calls.md
├── File Systems.md
├── Linux/
│   ├── Linux.md
│   ├── Linux Structure Proposal.md
│   ├── Linux Kernel.md
│   ├── Linux Distribution.md
│   ├── Linux File System.md
│   └── Linux File System Structure Proposal.md
├── Processes and Threads/
│   ├── Processes and Threads.md
│   ├── Processes and Threads Structure Proposal.md
│   ├── Thread.md
│   ├── Interprocess Communication.md
│   ├── Process/
│   │   ├── Process.md
│   │   └── Process State Model.md
│   ├── CPU Scheduling/
│   │   ├── CPU Scheduling.md
│   │   └── Context Switch.md
│   └── Synchronization Primitives/
│       ├── Synchronization Primitives.md
│       ├── Synchronization Primitives Structure Proposal.md
│       ├── Race Condition.md
│       └── Data Race.md
├── Virtual Memory/
│   ├── Virtual Memory.md
│   ├── Virtual Memory Structure Proposal.md
│   ├── Virtual Address Space.md
│   └── Paging/
│       ├── Paging.md
│       ├── Page Table.md
│       ├── TLB.md
│       └── Page Fault.md
└── Containerization/
    ├── Containerization.md
    ├── Docker.md
    └── Docker Structure Proposal.md
```

## Что не стоит создавать заранее

- `Kernel Mode and User Mode`
- `Interrupts`
- `Deadlock`
- `Container Runtime`
- `Linux Namespaces`
- `cgroups`
- `OCI`

Эти темы лучше выносить в отдельные заметки только по мере появления устойчивого корпуса.

## Что создано в Inbox

- `[[Operating Systems]]`
- `[[Processes and Threads]]`
- `[[Process]]`
- `[[Process State Model]]`
- `[[Thread]]`
- `[[CPU Scheduling]]`
- `[[Context Switch]]`
- `[[Interprocess Communication]]`
- `[[Synchronization Primitives]]`
- `[[Race Condition]]`
- `[[Data Race]]`
- `[[System Calls]]`
- `[[File Systems]]`
- `[[Linux]]`
- `[[Linux Kernel]]`
- `[[Linux Distribution]]`
- `[[Linux File System]]`
- `[[Virtual Memory]]`
- `[[Virtual Address Space]]`
- `[[Paging]]`
- `[[Page Table]]`
- `[[TLB]]`
- `[[Page Fault]]`
- `[[Containerization]]`
- `[[Docker]]`

## Что стоит раскрыть дальше

- [ ] Проверить согласованность секций `processes-and-threads`, `system-calls`, `file-systems`, `memory-management`, `linux` и `containerization`
- [ ] Проверить, когда Linux-ветка требует дополнительных Linux-specific article помимо `Linux File System`
- [ ] Проверить, когда `Containerization` начнет требовать отдельные дочерние статьи помимо `Docker`
- [ ] Проверить `related`