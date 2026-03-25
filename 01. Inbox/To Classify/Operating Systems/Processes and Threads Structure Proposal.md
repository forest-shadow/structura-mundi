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
  - "[[CPU Scheduling]]"
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
```

## Почему структура именно такая

- `Processes and Threads` уже оправдан как `sub-overview`, потому что внутри ветки есть не только две базовые сущности, но и отдельные механизмы исполнения и координации.
- `Process` и `Thread` остаются основными объяснительными article-notes про контейнер ресурсов и единицу исполнения.
- `Process State Model` логично подвешивать к `Process`, потому что она конкретизирует жизненный цикл исполняемой сущности и связывает его с readiness, blocking и termination.
- `CPU Scheduling` и `Context Switch` образуют естественную пару policy + mechanism.
- `Interprocess Communication` нужен как отдельный article, потому что изолированные процессы без него остаются только контейнерами, но не взаимодействующими агентами системы.
- `Synchronization Primitives` уже оправдан как отдельный article, потому что после появления `Thread` и `Interprocess Communication` возникает устойчивый слой координации concurrent execution.

## Что не стоит делать прямо сейчас

- Не стоит дробить ветку до отдельных notes про каждый scheduling algorithm.
- Не стоит преждевременно выделять `Kernel Mode and User Mode` и `Interrupts` внутрь этой подветки.
- Не стоит разносить language-level concurrency abstractions сюда же.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен `Deadlock`
- [ ] Решить, когда нужен отдельный article про `Thread State Model`
- [ ] Проверить `related`
