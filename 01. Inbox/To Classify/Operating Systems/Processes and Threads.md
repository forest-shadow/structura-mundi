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
  - "[[Thread]]"
  - "[[CPU Scheduling]]"
  - "[[System Calls]]"
tags: []
---

# Processes and Threads

## Краткое определение области

`Processes and Threads` — это обзорная заметка про execution-модель операционной системы: какие единицы работы она изолирует, как они выполняются и как именно процессорное время распределяется между ними.

## Что входит в эту тему

- `[[Process]]`
- `[[Thread]]`
- `[[CPU Scheduling]]`

## Как устроена ветка

- `Process` описывает изолированную единицу выполнения с собственными ресурсами и адресным пространством.
- `Thread` описывает более легковесную execution unit внутри процесса.
- `CPU Scheduling` объясняет, как ОС выбирает, кто именно выполняется на процессоре в каждый момент.

## Рекомендуемый маршрут чтения

1. Сначала прочитать `[[Process]]`.
2. Затем перейти к `[[Thread]]`.
3. После этого читать `[[CPU Scheduling]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Operating Systems]]`

## Что стоит раскрыть дальше

- [ ] Уточнить различие между process abstraction и thread abstraction
- [ ] Решить, нужен ли позже отдельный узел про synchronization
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
