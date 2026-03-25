---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Processes and Threads]]"
status: seed
related:
  - "[[Process State Model]]"
  - "[[Thread]]"
  - "[[CPU Scheduling]]"
  - "[[Interprocess Communication]]"
  - "[[Virtual Address Space]]"
tags: []
---

# Process

## Краткое определение

`Process` — это изолированная единица выполнения, которой операционная система выделяет собственное адресное пространство, ресурсы и контекст исполнения.

## Почему тема находится в ветке Processes and Threads

Эта заметка нужна как базовый уровень process model, от которого затем естественно переходить к `Thread` и к тому, как ОС планирует выполнение.

## Основная идея или механизм

- процесс инкапсулирует программу в исполнении;
- операционная система отслеживает его состояние и ресурсы;
- изоляция процесса тесно связана с его собственным virtual address space.

## Границы темы

- Входит: process как OS abstraction.
- Не входит: полный разбор IPC, synchronization primitives и всех моделей multitasking.

## Примеры, случаи или следствия

Эта заметка должна показать, почему процесс — это не просто "программа", а управляемый системный объект с собственным состоянием и памятью.

## Связи с другими заметками

Родительская тема:

`[[Processes and Threads]]`

Связанные заметки:

- `[[Thread]]`
- `[[Process State Model]]`
- `[[CPU Scheduling]]`
- `[[Interprocess Communication]]`
- `[[Virtual Address Space]]`

## Что стоит раскрыть дальше

- [ ] Уточнить разницу между process и program
- [ ] Добавить связь с адресным пространством процесса
- [ ] Проверить `related`
- [ ] Проверить `aliases`
