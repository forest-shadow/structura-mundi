---
aliases:
  - Concurrency in Go
  - Модель конкурентности Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Goroutines]]"
  - "[[Go Channels]]"
  - "[[Go Scheduler]]"
tags: []
---

# Go Concurrency Model

## Краткое определение области

Обзорная заметка для idiomatic concurrency-модели Go: goroutines, channels и способов координации конкурентного выполнения.

## Что входит в эту тему

- `[[Go Goroutines]]`
- `[[Go Channels]]`
- `[[Go Scheduler]]`

## Как устроена ветка

- Это оправданный `sub-overview`, потому что concurrency в Go образует плотную самостоятельную подветку.
- Внутри него сейчас достаточно трёх устойчивых узлов: про goroutines, channels и scheduler.
- Более глубокую вложенность стоит добавлять только по мере появления реального корпуса заметок.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи concurrency в Go.
2. Затем перейти к `[[Go Goroutines]]`.
3. После этого перейти к `[[Go Scheduler]]`, чтобы понять runtime side of concurrency.
4. Затем читать `[[Go Channels]]` как механизм координации.

## Соседние overview-ветки

- `[[Go]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужны ли отдельные заметки про `select`, `context` и synchronization primitives
- [ ] Проверить границы между `Go Scheduler` и `Go Goroutines`
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
- [ ] Уточнить границы с memory model
