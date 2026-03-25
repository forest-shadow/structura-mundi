---
aliases:
  - runtime.GOMAXPROCS
  - GOMAXPROCS Environment Variable
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler]]"
status: seed
related:
  - "[[Go Scheduler]]"
  - "[[Go Scheduler GMP Model]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Netpoller]]"
tags: []
---

# GOMAXPROCS

## Краткое определение

`GOMAXPROCS` — это runtime-параметр Go, который задает максимальное число логических процессоров `P`, одновременно допускаемых к исполнению Go-кода.

## Почему тема находится в ветке Go Scheduler

Эта заметка относится к `[[Go Scheduler]]`, потому что `GOMAXPROCS` управляет не количеством goroutines и не числом потоков ОС напрямую, а именно мощностью scheduler-модели `G-M-P` на уровне множества `P`.

## Основная идея или механизм

- `GOMAXPROCS` ограничивает степень реального параллелизма Go-кода;
- значение по умолчанию обычно привязывается к числу доступных логических CPU;
- параметр можно задать через переменную окружения `GOMAXPROCS` или изменить во время выполнения через `runtime.GOMAXPROCS`.

## Границы темы

- Входит: связь `GOMAXPROCS` с множеством `P`, scheduler behavior и CPU-bound workload.
- Не входит: полный разбор всех переменных рантайма Go, cgroup-aware autotuning и частные детали конкретных container environments.

## Связи с другими заметками

Родительская тема:

`[[Go Scheduler]]`

Связанные заметки:

- `[[Go Scheduler GMP Model]]`
- `[[Go Concurrency Model]]`
- `[[Go Netpoller]]`

## Примеры, случаи или следствия

- Увеличение `GOMAXPROCS` повышает верхнюю границу параллельного исполнения CPU-bound goroutines, но не увеличивает само количество goroutines.
- Слишком низкое значение может искусственно ограничивать throughput.
- Слишком высокое значение в средах с ограниченными CPU quota может ухудшать предсказуемость latency и планирования.

## Что стоит раскрыть дальше

- [ ] Развести `GOMAXPROCS`, количество goroutines и число OS threads
- [ ] Добавить примеры настройки через env var и `runtime.GOMAXPROCS`
- [ ] Уточнить связь с container CPU limits
- [ ] Проверить `aliases`
