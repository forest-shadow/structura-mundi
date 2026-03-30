---
aliases:
  - IPC
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Processes and Threads]]"
status: seed
related:
  - "[[Process]]"
  - "[[System Calls]]"
  - "[[Synchronization Primitives]]"
tags: []
---

# Interprocess Communication

## Краткое определение

`Interprocess Communication` — это статья о механизмах, через которые изолированные процессы обмениваются данными, событиями и сигналами координации.

## Почему тема находится в ветке Processes and Threads

Процессы в ОС по умолчанию изолированы. Поэтому IPC нужен как отдельный слой, объясняющий, как взаимодействие возникает поверх этой изоляции, а не вместо нее.

## Основная идея или механизм

- процесс не разделяет address space с другими процессами напрямую;
- обмен требует специальных OS-level mechanisms вроде pipes, message passing, shared memory или signals;
- выбор механизма влияет на стоимость взаимодействия, модель синхронизации и границы изоляции.

## Границы темы

- Входит: IPC как family of mechanisms для communication между process boundaries.
- Не входит: сетевое взаимодействие распределенных систем как отдельный уровень абстракции.

## Связи с другими заметками

Родительская тема:

`[[Processes and Threads]]`

Связанные заметки:

- `[[Process]]`
- `[[System Calls]]`
- `[[Synchronization Primitives]]`

## Примеры, случаи или следствия

- Pipe удобен как поток байтов между процессами, но не эквивалентен shared memory.
- Shared memory снижает стоимость копирования данных, но усиливает требования к синхронизации.

## Что стоит раскрыть дальше

- [ ] Уточнить, когда выделять отдельные notes про pipes, signals и shared memory
- [ ] Добавить связь с process isolation
- [ ] Проверить `related`
