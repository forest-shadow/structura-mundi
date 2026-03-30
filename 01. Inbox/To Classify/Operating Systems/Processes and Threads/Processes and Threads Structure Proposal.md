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

Предлагаемое устройство ветки `Processes and Threads` как подветки execution model внутри `Operating Systems`.

## Рекомендуемая иерархия

```text
Operating Systems
└── Processes and Threads
    ├── Process
    │   └── Process State Model
    ├── Thread
    ├── CPU Scheduling
    │   └── Context Switch
    ├── Interprocess Communication
    └── Synchronization Primitives
        ├── Race Condition
        └── Data Race
```

## Почему структура именно такая

- `Processes and Threads` уже оправдан как `sub-overview`, потому что внутри ветки есть не только базовые сущности, но и отдельные механизмы исполнения и координации.
- `Process` и `Thread` остаются основными explanatory articles про контейнер ресурсов и единицу исполнения.
- `Process State Model` логично подвешивать к `Process`, потому что она конкретизирует жизненный цикл исполняемой сущности и связывает его с readiness, blocking и termination.
- `CPU Scheduling` и `Context Switch` образуют естественную пару policy + mechanism.
- `Interprocess Communication` нужен как отдельный article, потому что изолированные процессы без него остаются только контейнерами, но не взаимодействующими агентами системы.
- `Synchronization Primitives` теперь оправдан как локальный `sub-overview`, потому что внутри него уже есть устойчивый кластер из coordination mechanisms и failure modes concurrent execution.
- `Race Condition` фиксирует общий correctness-level класс сбоев, зависящих от относительного порядка interleaving.
- `Data Race` остаётся обычной `article` рядом с `Race Condition`, а не подвешивается под неё, чтобы ветка оставалась максимально плоской.

## Текущая физическая раскладка в Inbox

```text
Processes and Threads/
├── Processes and Threads.md
├── Processes and Threads Structure Proposal.md
├── Thread.md
├── Interprocess Communication.md
├── Process/
│   ├── Process.md
│   └── Process State Model.md
├── CPU Scheduling/
│   ├── CPU Scheduling.md
│   └── Context Switch.md
└── Synchronization Primitives/
    ├── Synchronization Primitives.md
    ├── Synchronization Primitives Structure Proposal.md
    ├── Race Condition.md
    └── Data Race.md
```

## Что не стоит делать прямо сейчас

- Не стоит дробить ветку до отдельных notes про каждый scheduling algorithm.
- Не стоит преждевременно выделять `Kernel Mode and User Mode` и `Interrupts` внутрь этой подветки.
- Не стоит разносить language-level concurrency abstractions сюда же.
- Не стоит заводить отдельный `Concurrency Hazards` overview, пока кластер нормально читается через `Synchronization Primitives`.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Mutex`, `Semaphore` и `Condition Variable`
- [ ] Решить, когда нужен `Deadlock`
- [ ] Решить, когда нужен отдельный article про `Thread State Model`
- [ ] Проверить `related`
