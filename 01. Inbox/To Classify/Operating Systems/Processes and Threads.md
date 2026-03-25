---
aliases: []
note_type: overview
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Operating Systems]]"
status: seed
related:
  - "[[Process]]"
  - "[[Process State Model]]"
  - "[[Thread]]"
  - "[[CPU Scheduling]]"
  - "[[Context Switch]]"
  - "[[Interprocess Communication]]"
  - "[[Synchronization Primitives]]"
tags: []
---

# Processes and Threads

## Краткое определение области

`Processes and Threads` — это обзорная заметка про execution-модель операционной системы: какие единицы работы она изолирует, как они выполняются и как именно процессорное время распределяется между ними.

## Что входит в эту тему

- `[[Process]]`
- `[[Process State Model]]`
- `[[Thread]]`
- `[[CPU Scheduling]]`
- `[[Context Switch]]`
- `[[Interprocess Communication]]`
- `[[Synchronization Primitives]]`

## Как устроена ветка

- `Process` описывает изолированную единицу выполнения с собственными ресурсами и адресным пространством.
- `Process State Model` уточняет, через какие состояния проходит исполняемая единица и как это связано с планированием.
- `Thread` описывает более легковесную execution unit внутри процесса.
- `CPU Scheduling` объясняет, как ОС выбирает, кто именно выполняется на процессоре в каждый момент.
- `Context Switch` связывает scheduling с реальной сменой исполняемого контекста на CPU.
- `Interprocess Communication` описывает, как изолированные процессы обмениваются данными и координируют работу.
- `Synchronization Primitives` собирает базовые механизмы координации concurrent execution внутри и между процессами.

## Рекомендуемый маршрут чтения

1. Сначала прочитать `[[Process]]` и `[[Process State Model]]`.
2. Затем перейти к `[[Thread]]`.
3. После этого читать `[[CPU Scheduling]]` и `[[Context Switch]]`.
4. Завершить `[[Interprocess Communication]]` и `[[Synchronization Primitives]]` как coordination layer этой ветки.

## Соседние overview-ветки

- Родительская рамка: `[[Operating Systems]]`

## Что стоит раскрыть дальше

- [ ] Уточнить различие между process abstraction и thread abstraction
- [ ] Решить, когда рядом понадобятся `Deadlock` и более узкие synchronization notes
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
