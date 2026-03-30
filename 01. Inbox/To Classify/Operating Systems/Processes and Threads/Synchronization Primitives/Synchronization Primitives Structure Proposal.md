---
aliases:
  - Synchronization Primitives Structure Proposal
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Synchronization Primitives]]"
status: draft
related:
  - "[[Synchronization Primitives]]"
  - "[[Processes and Threads]]"
  - "[[Race Condition]]"
  - "[[Data Race]]"
tags: []
---

# Synchronization Primitives Structure Proposal

## Краткое определение

Предлагаемое устройство локальной ветки `Synchronization Primitives` внутри `Processes and Threads`, в которую естественно помещаются заметки про `Race Condition` и `Data Race`.

## Рекомендуемая иерархия

```text
Operating Systems
└── Processes and Threads
    └── Synchronization Primitives
        ├── Race Condition
        └── Data Race
```

## Почему структура именно такая

- `Synchronization Primitives` уже перестал быть одной isolated article и теперь оправдан как локальный обзорный узел про coordination layer concurrent execution.
- `Race Condition` нужен как обычный `article`, потому что это устойчивое общее понятие про ошибку, зависящую от порядка interleaving.
- `Data Race` нужен как отдельный `article`, потому что это более узкий memory-level случай, который требует собственной границы темы.
- `Data Race` лучше пока держать рядом с `Race Condition`, а не под ним, чтобы не делать лишний уровень вложенности.

## Текущая физическая раскладка в Inbox

```text
Synchronization Primitives/
├── Synchronization Primitives.md
├── Synchronization Primitives Structure Proposal.md
├── Race Condition.md
└── Data Race.md
```

## Что не стоит создавать заранее

- Не стоит заводить отдельный `Concurrency Hazards` overview.
- Не стоит сразу выносить `Mutex`, `Semaphore`, `Condition Variable` и `Deadlock` в отдельные notes без устойчивого наполнения.
- Не стоит смешивать сюда language-specific memory model notes.

## Что создано в Inbox

- `[[Synchronization Primitives]]`
- `[[Race Condition]]`
- `[[Data Race]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда ветка требует отдельных notes про concrete primitives
- [ ] Решить, когда понадобится `Deadlock`
- [ ] Проверить `related`
