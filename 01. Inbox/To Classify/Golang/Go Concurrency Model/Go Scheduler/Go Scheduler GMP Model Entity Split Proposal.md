---
aliases:
  - GMP Entity Split Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler GMP Model]]"
status: draft
related:
  - "[[Go Scheduler GMP Model]]"
  - "[[Go Machine Thread]]"
  - "[[Go Scheduler Processor]]"
  - "[[Go Goroutines]]"
tags: []
---

# Go Scheduler GMP Model Entity Split Proposal

## Краткое определение

Предлагаемое расширение ветки `Go Scheduler GMP Model`, в котором сущности `M` и `P` выносятся в самостоятельные канонические статьи, а `G` остаётся покрыт существующей заметкой `[[Go Goroutines]]`.

## Почему это полезно

- `G`, `M` и `P` в модели `G-M-P` являются не просто буквами, а разными объектами знания.
- При этом отдельные статьи на буквы были бы слишком абстрактными и плохо соответствовали бы правилам именования.
- Канонические имена `Go Machine Thread` и `Go Scheduler Processor` делают ветку точнее без лишнего дробления.

## Рекомендуемая иерархия

```text
Go
└── Go Concurrency Model
    └── Go Scheduler GMP Model
        ├── Go Goroutines
        ├── Go Machine Thread
        └── Go Scheduler Processor
```

## Почему структура именно такая

- `Go Goroutines` уже фактически покрывает сущность `G`, поэтому отдельная заметка на `G` не нужна.
- `Go Machine Thread` оправдан как статья про OS-thread carrier, blocking syscalls и взаимодействие с runtime.
- `Go Scheduler Processor` оправдан как статья про логический ресурс исполнения, local run queue и смысл `GOMAXPROCS`.

## Что не стоит делать сейчас

- Не стоит создавать заметки `G.md`, `M.md` и `P.md`.
- Не стоит сразу дробить `Go Scheduler Processor` на allocator caches, per-P queues и прочие внутренности runtime.
- Не стоит дублировать уже существующую тему `[[Go Goroutines]]`.

## Что уже создано в Inbox

- `[[Go Machine Thread]]`
- `[[Go Scheduler Processor]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, нужно ли в будущем отдельно выделять `LockOSThread`
- [ ] Проверить связь между `Go Scheduler Processor` и `GOMAXPROCS`
- [ ] Проверить `related`
