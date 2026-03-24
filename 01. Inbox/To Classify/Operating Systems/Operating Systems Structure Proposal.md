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
tags: []
---

# Operating Systems Structure Proposal

## Краткое определение

Предлагаемая ветка для `Operating Systems` собирает под одним корневым обзорным узлом базовые механизмы ОС: процессную модель, системные вызовы, файловые системы и memory-management ветку `Virtual Memory`.

## Выбранная оптика

- `area: computer-science`
- `domain: operating-systems` (предлагаемое новое значение)
- `section:` пусто у domain-root overview `Operating Systems`

Почему так:

- тема не укладывается естественно в уже подтвержденные `domain`;
- для ОС нужен собственный предметный фокус, а не искусственное размещение в `system-design`;
- корневая заметка `Operating Systems` описывает весь `domain`, поэтому по обновленным правилам не должна получать служебный `section`;
- дочерние кластеры уже получают собственные смысловые секции: `processes-and-threads`, `system-calls`, `file-systems`, `memory-management`.

## Каноническое имя

- корневая обзорная заметка: `Operating Systems`
- `OS` и `Operating System` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Operating Systems
├── Processes and Threads
│   ├── Process
│   ├── Thread
│   └── CPU Scheduling
├── System Calls
├── File Systems
└── Virtual Memory
    ├── Virtual Address Space
    └── Paging
        ├── Page Table
        ├── TLB
        └── Page Fault
```

## Почему структура именно такая

- `Operating Systems` нужен как root `overview`, потому что рядом уже возникают несколько самостоятельных смысловых кластеров, а не одна isolated article.
- `Processes and Threads` оправдан как `sub-overview`, потому что внутри него естественно живут `Process`, `Thread` и `CPU Scheduling`.
- `Virtual Memory` уже оправдан как отдельный `sub-overview`, потому что внутри него есть собственная плотная подветка.
- `System Calls` и `File Systems` пока разумнее держать как обычные `article`, чтобы не усложнять ветку раньше времени.

## Что не стоит создавать заранее

- `Kernel Mode and User Mode`
- `Context Switch`
- `Interrupts`
- `Synchronization Primitives`
- `Deadlock`
- `Inode`
- `Journaling File System`

Эти темы лучше выносить в отдельные заметки только по мере появления устойчивого корпуса.

## Предлагаемое физическое размещение после нормализации

```text
02. Corpus Mundi/
├── C/
│   └── CPU Scheduling.md
├── F/
│   └── File Systems.md
├── O/
│   └── Operating Systems.md
├── P/
│   ├── Process.md
│   ├── Processes and Threads.md
│   └── Page Table.md
├── S/
│   └── System Calls.md
├── T/
│   ├── Thread.md
│   └── TLB.md
└── V/
    ├── Virtual Address Space.md
    └── Virtual Memory.md
```

Логическая ветка при этом собирается через `parent`, а не через физическое соседство файлов.

## Что создано в Inbox

- `[[Operating Systems]]`
- `[[Processes and Threads]]`
- `[[Process]]`
- `[[Thread]]`
- `[[CPU Scheduling]]`
- `[[System Calls]]`
- `[[File Systems]]`
- `[[Virtual Memory]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: operating-systems`
- [ ] Проверить, что `Operating Systems` остается domain-root overview без `section`
- [ ] Проверить согласованность секций `processes-and-threads`, `system-calls`, `file-systems`, `memory-management`
- [ ] Проверить, когда `System Calls` и `File Systems` начнут требовать собственные sub-overview
- [ ] Проверить `related`
