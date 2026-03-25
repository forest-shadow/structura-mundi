---
aliases:
  - Golang Memory Management Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: draft
related:
  - "[[Go Memory Management]]"
  - "[[Go Escape Analysis]]"
  - "[[Go]]"
tags: []
---

# Go Memory Management Structure Proposal

## Краткое определение

Предлагаемое место для `Go Memory Management` внутри ветки `Go` как отдельного `sub-overview`, собирающего memory-related topics вокруг allocation behavior, runtime memory costs и garbage collection.

## Рекомендуемая иерархия

```text
Go
├── Go Toolchain
├── Go Packages and Modules
├── Go Type System
│   └── Go Interfaces
├── Go Error Handling
├── Go Memory Management
│   ├── Go Stack and Heap Allocation
│   ├── Go Escape Analysis
│   └── Go Garbage Collection
├── Go Concurrency Model
│   ├── Go Goroutines
│   ├── Go Channels
│   └── Go Scheduler
│       ├── Go Scheduler GMP Model
│       │   ├── Go Scheduler Processor
│       │   └── Go Machine Thread
│       ├── GOMAXPROCS
│       ├── Go Scheduler Work Stealing
│       ├── Go Scheduler Preemption
│       └── Go Netpoller
└── Go Testing
```

## Почему структура именно такая

- `Go Memory Management` уже достаточно широк для собственного `overview`: тема не сводится только к `Go Escape Analysis`.
- `Go Stack and Heap Allocation` нужен как базовая article-note о модели размещения значений.
- `Go Escape Analysis` логично сделать дочерней note, потому что это не общая вершина ветки, а один из механизмов внутри memory-management cluster.
- `Go Garbage Collection` нужен как отдельная article-note, потому что GC pressure, write barriers и runtime cost образуют самостоятельный слой вопросов.
- `Go Memory Model` сюда напрямую не входит: это соседняя тема про visibility и happens-before, а не про allocation и reclamation.

## Что не стоит делать прямо сейчас

- Не стоит смешивать `Go Memory Management` с `Go Memory Model`.
- Не стоит создавать специализированные шаблоны под memory notes.
- Не стоит дробить ветку глубже, пока не появились устойчивые notes вроде allocator internals или write barriers как самостоятельных тем.

## Что уже создано в Inbox

- `[[Go Memory Management]]`
- `[[Go Stack and Heap Allocation]]`
- `[[Go Escape Analysis]]`
- `[[Go Garbage Collection]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен `Go Memory Model`
- [ ] Уточнить, когда рядом появится `Go Allocator`
- [ ] Проверить `related`
