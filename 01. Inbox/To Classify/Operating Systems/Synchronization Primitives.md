---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Processes and Threads]]"
status: seed
related:
  - "[[Thread]]"
  - "[[Interprocess Communication]]"
  - "[[CPU Scheduling]]"
tags: []
---

# Synchronization Primitives

## Краткое определение

`Synchronization Primitives` — это статья о базовых механизмах координации concurrent execution: mutex, semaphore, condition variable и других средствах управления доступом к разделяемым ресурсам.

## Почему тема находится в ветке Processes and Threads

Эта заметка относится к ветке execution model, потому что конкурирующие потоки и процессы нуждаются не только в планировании, но и в безопасной координации доступа к общим данным и событиям.

## Основная идея или механизм

- concurrent execution создаёт риск races, lost updates и неконсистентного доступа к общему состоянию;
- synchronization primitives вводят правила взаимного исключения, ожидания и пробуждения;
- они связывают scheduling, blocking и coordination behavior в единую operational model.

## Границы темы

- Входит: базовые synchronization mechanisms и их роль в ОС и системном программировании.
- Не входит: полный формальный разбор lock-free algorithms и language-specific concurrency frameworks.

## Связи с другими заметками

Родительская тема:

`[[Processes and Threads]]`

Связанные заметки:

- `[[Thread]]`
- `[[Interprocess Communication]]`
- `[[CPU Scheduling]]`

## Примеры, случаи или следствия

- Shared memory без synchronization быстро приводит к race conditions.
- Blocking primitive влияет не только на correctness, но и на scheduler-visible behavior потока.

## Что стоит раскрыть дальше

- [ ] Решить, когда выделять `Mutex`, `Semaphore` и `Deadlock`
- [ ] Уточнить связь между blocking synchronization и scheduling
- [ ] Проверить `related`
