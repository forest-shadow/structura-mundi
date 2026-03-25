---
aliases:
  - Memory Management in Go
  - Управление памятью в Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Escape Analysis]]"
  - "[[Go Concurrency Model]]"
tags: []
---

# Go Memory Management

## Краткое определение области

Обзорная заметка про то, как в Go организованы размещение значений в памяти, аллокации, работа сборщика мусора и компиляторные решения, влияющие на стоимость исполнения.

## Что входит в эту тему

- `[[Go Stack and Heap Allocation]]`
- `[[Go Escape Analysis]]`
- `[[Go Garbage Collection]]`

## Как устроена ветка

- `Go Memory Management` оправдан как вложенный `overview`, потому что здесь уже есть не одна isolated note, а небольшой устойчивый кластер тем про allocation behavior и lifetime значений.
- `Go Escape Analysis` раскрывает компиляторное решение о том, что может остаться на стеке, а что должно уйти в кучу.
- `Go Stack and Heap Allocation` фиксирует базовую карту размещения значений и различие между stack и heap в Go runtime.
- `Go Garbage Collection` собирает темы про GC cycles, pressure, паузы, write barriers и практические следствия для production-кода.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Stack and Heap Allocation]]`, чтобы зафиксировать базовые различия между областями памяти.
2. Затем перейти к `[[Go Escape Analysis]]`, чтобы понять, почему компилятор принимает те или иные решения о размещении.
3. После этого читать `[[Go Garbage Collection]]` как тему про последствия allocation patterns для runtime.
4. Затем уже возвращаться к соседним runtime-веткам вроде `[[Go Scheduler]]`, если нужен полный operational context.

## Соседние overview-ветки

- `[[Go Concurrency Model]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между memory management и memory model
- [ ] Решить, нужен ли отдельный article про Go allocator internals
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
