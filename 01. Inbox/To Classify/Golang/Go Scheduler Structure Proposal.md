---
aliases:
  - Golang Scheduler Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Concurrency Model]]"
status: draft
related:
  - "[[Go Scheduler]]"
  - "[[Go Goroutines]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Netpoller]]"
tags: []
---

# Go Scheduler Structure Proposal

## Краткое определение

Предлагаемая ветка для `Go Scheduler` встраивает планировщик Go в уже существующую concurrency-подветку и раскладывает его на несколько самостоятельных аспектов, которые полезны энциклопедически.

## Почему тема заслуживает собственной подветки

- `Go Scheduler` не сводится просто к goroutines: это отдельный механизм рантайма, который определяет, как goroutines распределяются по потокам и процессорам.
- Тема достаточно плотная, чтобы быть не просто разделом внутри `[[Go Goroutines]]`, а отдельным узлом.
- При этом глубину стоит держать минимальной: достаточно одного `overview` и небольшого набора дочерних `article`.

## Рекомендуемая иерархия

```text
Go
└── Go Concurrency Model
    ├── Go Goroutines
    ├── Go Channels
    └── Go Scheduler
        ├── Go Scheduler GMP Model
        ├── Go Scheduler Work Stealing
        ├── Go Scheduler Preemption
        └── Go Netpoller
```

## Почему структура именно такая

- `Go Scheduler` лучше делать `overview`, потому что он объединяет несколько разных аспектов одного механизма.
- `Go Scheduler GMP Model` нужен как статья про базовую архитектурную модель `G-M-P`.
- `Go Scheduler Work Stealing` нужен как статья про ключевой способ балансировки нагрузки.
- `Go Scheduler Preemption` нужен как статья про то, как рантайм возвращает управление и избегает monopolization CPU.
- `Go Netpoller` нужен как статья про интеграцию scheduler с неблокирующим сетевым I/O и пробуждением goroutines.

## Что не стоит добавлять прямо сейчас

- Не стоит сразу делать отдельные статьи про каждый внутренний runtime queue или все детали sysmon.
- Не стоит превращать ветку в каталог исходников рантайма без устойчивых энциклопедических тем.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── G/
    ├── Go Scheduler.md
    ├── Go Scheduler GMP Model.md
    ├── Go Scheduler Work Stealing.md
    ├── Go Scheduler Preemption.md
    └── Go Netpoller.md
```

## Что уже создано в Inbox

- `[[Go Scheduler]]`
- `[[Go Scheduler GMP Model]]`
- `[[Go Scheduler Work Stealing]]`
- `[[Go Scheduler Preemption]]`
- `[[Go Netpoller]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужна ли отдельная статья про `sysmon`
- [ ] Решить, нужно ли выносить scheduler/GC interaction в отдельную заметку
- [ ] Уточнить связь между scheduler, netpoller и runtime timers
- [ ] Уточнить границы между `Go Goroutines` и `Go Scheduler`
- [ ] Проверить `related`
