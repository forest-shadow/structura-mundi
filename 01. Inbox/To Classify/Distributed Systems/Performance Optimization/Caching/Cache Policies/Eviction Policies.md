---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Cache Policies]]"
status: seed
related:
  - "[[Cache Policies]]"
  - "[[Expiration Policies]]"
  - "[[Admission Policies]]"
tags: []
---

# Eviction Policies

## Краткое определение

`Eviction Policies` — это статья о правилах, по которым кэш выбирает, какие объекты удалить при ограниченной ёмкости.

## Границы темы

- Входит: LRU, LFU, FIFO, random replacement и их смысловые trade-offs.
- Не входит: invalidation как реакция на изменение данных.

## Связи с другими заметками

Родительская тема:

`[[Cache Policies]]`

Связанные заметки:

- `[[Expiration Policies]]`
- `[[Admission Policies]]`
- `[[Cache Stampede]]`

## Примеры, случаи или следствия

- LRU хорошо работает там, где recent access предсказывает скорое повторное использование.
- Неподходящая eviction policy может уничтожать hit rate даже при большом cache size.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные articles про `LRU` и `LFU`
- [ ] Проверить `related`
