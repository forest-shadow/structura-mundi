---
aliases: []
note_type: overview
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Processes and Threads]]"
status: seed
related:
  - "[[Thread]]"
  - "[[Interprocess Communication]]"
  - "[[Race Condition]]"
  - "[[Data Race]]"
tags: []
---

# Synchronization Primitives

## Краткое определение области

`Synchronization Primitives` — это обзорная заметка о базовых механизмах координации concurrent execution: mutual exclusion, ordering, waiting и signaling, а также о типичных сбоях, которые возникают при доступе к общему состоянию без этих механизмов.

## Что входит в эту тему

- `[[Race Condition]]`
- `[[Data Race]]`
- базовые primitive-level механизмы вроде mutex, semaphore и condition variable
- связь между synchronization, scheduling и shared state

## Как устроена ветка

- `Race Condition` описывает общий класс ошибок, где результат зависит от относительного порядка interleaving.
- `Data Race` фиксирует более узкий случай несинхронизированного доступа к одной и той же области памяти.
- сами synchronization primitives лучше держать в этой ветке как механизмы предотвращения сбоев, а не смешивать их с language-specific concurrency frameworks.

## Рекомендуемый маршрут чтения

1. Начать с `[[Race Condition]]`, чтобы зафиксировать сам класс проблемы.
2. Затем перейти к `[[Data Race]]` как к более узкому memory-level случаю.
3. После этого возвращаться к конкретным primitives и их роли в предотвращении этих сбоев.

## Соседние overview-ветки

- Родительская рамка: `[[Processes and Threads]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда выделять `Mutex`, `Semaphore` и `Condition Variable`
- [ ] Решить, когда внутри ветки понадобится отдельный article про `Deadlock`
- [ ] Уточнить связь между synchronization, scheduling и memory ordering
- [ ] Проверить `related`
