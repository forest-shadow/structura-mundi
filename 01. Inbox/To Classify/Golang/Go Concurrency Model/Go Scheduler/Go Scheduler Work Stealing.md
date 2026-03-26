---
aliases:
  - Work Stealing in Go Scheduler
  - Work Stealing in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler]]"
status: draft
related:
  - "[[Go Scheduler]]"
  - "[[Go Scheduler GMP Model]]"
  - "[[Go Goroutines]]"
tags: []
---

# Go Scheduler Work Stealing

## Краткое определение

Статья о work stealing как одном из ключевых механизмов балансировки нагрузки в планировщике Go.

## Основная идея или механизм

Когда локальная очередь работы одного логического процессора опустела, планировщик может забирать часть работы у другого, чтобы лучше использовать доступный параллелизм.

## Границы темы

- В тему входит логика перераспределения runnable goroutines между очередями.
- На границе находятся более общие идеи scheduler architecture и preemption.

## Связи с другими заметками

Родительская тема:

`[[Go Scheduler]]`

Связанные заметки:

- `[[Go Scheduler GMP Model]]`
- `[[Go Goroutines]]`

## Примеры, случаи или следствия

Work stealing помогает избегать ситуаций, когда часть процессоров простаивает, а работа концентрируется в одной локальной очереди.

## Что стоит раскрыть дальше

- [ ] Уточнить роль local and global run queues
- [ ] Добавить практические следствия для производительности
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
