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
│   │   └── Process State Model
│   ├── Thread
│   ├── CPU Scheduling
│   │   └── Context Switch
│   ├── Interprocess Communication
│   └── Synchronization Primitives
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
- `Processes and Threads` оправдан как `sub-overview`, потому что внутри него уже живут не только `Process`, `Thread` и `CPU Scheduling`, но и отдельные coordination/mechanism notes.
- `Virtual Memory` уже оправдан как отдельный `sub-overview`, потому что внутри него есть собственная плотная подветка.
- `System Calls` и `File Systems` пока разумнее держать как обычные `article`, чтобы не усложнять ветку раньше времени.

## Что не стоит создавать заранее

- `Kernel Mode and User Mode`
- `Interrupts`
- `Deadlock`
- `Inode`
- `Journaling File System`

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
- `[[System Calls]]`
- `[[File Systems]]`
- `[[Virtual Memory]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: operating-systems`
- [ ] Проверить, что `Operating Systems` остается domain-root overview без `section`
- [ ] Проверить согласованность секций `processes-and-threads`, `system-calls`, `file-systems`, `memory-management`
- [ ] Проверить, когда `System Calls` и `File Systems` начнут требовать собственные sub-overview
- [ ] Проверить, когда внутри `Processes and Threads` понадобятся `Deadlock` и `Interrupts`
- [ ] Проверить `related`

# OS: Структура предметной области (Топология ветки)

Ветка `Operating Systems` организована вокруг ключевых системных механизмов и содержит следующие дочерние узлы:
- `[[Processes and Threads]]`: Базовая модель исполнения. Включает контекст процесса, состояния, алгоритмы планировщика, конкурентность, переключение контекста и синхронизацию.
  Сейчас канонический минимум ветки: `Process`, `Process State Model`, `Thread`, `CPU Scheduling`, `Context Switch`, `Interprocess Communication`, `Synchronization Primitives`.
- `[[System Calls]]`: Граница взаимодействия user/kernel space. Включает механизм программных прерываний, ABI, передачу аргументов через регистры и стоимость вызовов.
- `[[File Systems]]`: Организация долговременного персистентного хранения. Раскрывает концепции пространства имён, inode, виртуальной файловой системы (VFS), кэширования (page cache) и журналирования.
- `[[Virtual Memory]]`: Подветка управления памятью с глубокой вложенностью. Собирает концепции таблиц страниц (Page Tables), TLB, сегментации, `mmap`, `page fault`, `copy-on-write` и подкачки.

## Рекомендуемый маршрут чтения

1. Начать с `[[Processes and Threads]]` для фиксации фундаментальной модели исполнения и отличий контейнера ресурсов (процесса) от единицы планирования (потока).
2. Перейти к `[[System Calls]]`, чтобы проследить механизм запроса сервисов процессами у привилегированного ядра.
3. Изучить `[[Virtual Memory]]` для понимания механизмов изоляции процессов, трансляции адресов, `page fault` и поведения физической памяти.
4. Завершить `[[File Systems]]`, связывая модель памяти и процессов с долговременным вводом-выводом и отображением файлов.
