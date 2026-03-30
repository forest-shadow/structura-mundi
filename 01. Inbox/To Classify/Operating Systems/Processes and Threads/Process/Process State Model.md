---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Process]]"
status: seed
related:
  - "[[Process]]"
  - "[[CPU Scheduling]]"
  - "[[Context Switch]]"
tags: []
---

# Process State Model

## Краткое определение

`Process State Model` — это статья о канонической модели состояний процесса: как ОС различает creation, readiness, execution, blocking и termination исполняемой сущности.

## Почему тема находится в ветке Processes and Threads

Эта заметка уточняет не общую идею процесса как контейнера ресурсов, а его динамическое поведение во времени. Поэтому она естественно продолжает `[[Process]]` и связывает его с `[[CPU Scheduling]]`.

## Основная идея или механизм

- процесс не просто существует, а проходит через набор операционных состояний;
- переходы между состояниями определяются событиями вроде запуска, истечения кванта, ожидания I/O и завершения;
- именно эта модель делает понятными ready queues, blocking и повторный выбор процесса планировщиком.

## Границы темы

- Входит: canonical process lifecycle и переходы между состояниями.
- Не входит: детальный разбор всех vendor-specific state diagrams и реализаций конкретных ОС.

## Связи с другими заметками

Родительская тема:

`[[Process]]`

Связанные заметки:

- `[[CPU Scheduling]]`
- `[[Context Switch]]`
- `[[Thread]]`

## Примеры, случаи или следствия

- Без state model трудно объяснить, почему процесс может быть существующим, но не исполняющимся.
- Blocking на I/O показывает, что остановка исполнения не тождественна завершению процесса.

## Что стоит раскрыть дальше

- [ ] Уточнить, когда рядом нужен `Thread State Model`
- [ ] Добавить связь с ready queue и waiting queue
- [ ] Проверить `related`
