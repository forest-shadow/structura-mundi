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
  - "[[CPU Scheduling]]"
  - "[[Context Switch]]"
  - "[[Synchronization Primitives]]"
  - "[[System Calls]]"
tags: []
---

# Thread

## Краткое определение

`Thread` — это более легковесная единица выполнения внутри процесса, которая разделяет с другими потоками процесса часть общих ресурсов, но имеет собственный execution context.

## Почему тема находится в ветке Processes and Threads

Эта заметка нужна как второй базовый узел process model: без нее невозможно ясно объяснить, что именно планирует ОС и что именно делят единицы выполнения внутри процесса.

## Основная идея или механизм

- поток живет внутри процесса;
- потоки одного процесса разделяют часть общей памяти и ресурсов;
- планирование CPU обычно работает именно с runnable execution units вроде threads.

## Границы темы

- Входит: thread как OS-level execution abstraction.
- Не входит: полный разбор user-level threads, coroutines и language runtime scheduling.

## Примеры, случаи или следствия

Эта заметка должна показать, почему многопоточность уменьшает стоимость параллельного исполнения по сравнению с множеством независимых процессов, но усложняет координацию и доступ к общей памяти.

## Связи с другими заметками

Родительская тема:

`[[Processes and Threads]]`

Связанные заметки:

- `[[Process]]`
- `[[CPU Scheduling]]`
- `[[Context Switch]]`
- `[[Synchronization Primitives]]`
- `[[System Calls]]`

## Что стоит раскрыть дальше

- [ ] Уточнить различие между thread и process context
- [ ] Развести OS threads и user-level abstractions
- [ ] Проверить `related`
- [ ] Проверить `aliases`
