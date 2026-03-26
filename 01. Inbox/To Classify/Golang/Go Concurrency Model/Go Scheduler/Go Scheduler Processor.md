---
aliases:
  - Processor in GMP Model
  - P in GMP Model
  - Go P
  - Logical Processor in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler GMP Model]]"
status: draft
related:
  - "[[Go Scheduler GMP Model]]"
  - "[[Go Machine Thread]]"
  - "[[Go Goroutines]]"
  - "[[Go Scheduler Work Stealing]]"
tags: []
---

# Go Scheduler Processor

## Краткое определение

Статья о сущности `P` в модели `G-M-P`: логическом ресурсе рантайма Go, который даёт право выполнять Go-код и содержит локальное состояние планировщика.

## Основная идея или механизм

`Go Scheduler Processor` не является ни goroutine, ни OS thread. Это runtime-абстракция, вокруг которой организуются local run queue, часть allocator state и верхняя граница истинного параллелизма Go-кода.

## Границы темы

- В тему входит роль `P` как логического процессора и контейнера локальных ресурсов scheduler.
- На границе находятся `M` как системный поток и более общие вопросы concurrency model.

## Связи с другими заметками

Родительская тема:

`[[Go Scheduler GMP Model]]`

Связанные заметки:

- `[[Go Machine Thread]]`
- `[[Go Goroutines]]`
- `[[Go Scheduler Work Stealing]]`

## Примеры, случаи или следствия

Эта тема объясняет, почему `GOMAXPROCS` ограничивает именно число одновременно исполняемых goroutines, а не число созданных потоков или самих goroutines.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между `P`, local run queue и `GOMAXPROCS`
- [ ] Проверить, нужна ли отдельная статья про per-P local resources
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
