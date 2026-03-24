---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Processes and Threads]]"
status: seed
related:
  - "[[Process]]"
  - "[[Thread]]"
tags: []
---

# CPU Scheduling

## Краткое определение

`CPU Scheduling` — это механизм, через который операционная система выбирает, какой процесс или поток получает процессорное время в текущий момент.

## Почему тема находится в ветке Processes and Threads

Эта заметка относится к execution model OS, потому что scheduling определяет динамику выполнения процессов и потоков, а не memory-management или storage.

## Основная идея или механизм

- runnable units конкурируют за CPU;
- scheduler выбирает следующего исполнителя по определенной политике;
- это влияет на latency, throughput и perceived responsiveness системы.

## Границы темы

- Входит: scheduling как OS-level policy and mechanism.
- Не входит: полный разбор всех алгоритмов планирования и scheduler implementation details конкретных ОС.

## Примеры, случаи или следствия

Эта заметка должна показать, почему performance системы зависит не только от быстроты CPU, но и от того, как ОС распределяет время между competing tasks.

## Связи с другими заметками

Родительская тема:

`[[Processes and Threads]]`

Связанные заметки:

- `[[Process]]`
- `[[Thread]]`

## Что стоит раскрыть дальше

- [ ] Развести preemptive и cooperative scheduling
- [ ] Добавить связь с context switch
- [ ] Проверить `related`
- [ ] Проверить `aliases`
