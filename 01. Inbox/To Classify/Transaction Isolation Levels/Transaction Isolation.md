---
aliases: []
note_type: overview
area: computer-science
domain: databases
section: transactions
parent: "[[ACID]]"
status: draft
related:
  - "[[ACID]]"
  - "[[Database Transactions]]"
  - "[[Transaction Isolation Levels]]"
  - "[[Isolation Anomalies]]"
tags:
  - transactions
  - consistency
---

# Transaction Isolation

## Краткое определение области

Обзорная заметка для свойства isolation в транзакционной модели: какие аномалии оно предотвращает и как это выражается в конкретных уровнях изоляции.

## Что входит в эту тему

- `[[Isolation Anomalies]]`
- `[[Transaction Isolation Levels]]`

## Как устроена ветка

- `Transaction Isolation` описывает само свойство isolation как часть `ACID`.
- Детальная шкала компромиссов вынесена в `[[Transaction Isolation Levels]]`.
- Дополнительная вложенность оправдана, потому что уровни изоляции образуют самостоятельную обзорную подветку.

## Рекомендуемый маршрут чтения

1. Понять isolation как свойство `ACID`.
2. Перейти к `[[Isolation Anomalies]]`.
3. Затем изучить `[[Transaction Isolation Levels]]` и его дочерние статьи.

## Соседние overview-ветки

- `[[ACID]]`
- `[[Database Transactions]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, какие аномалии считаются базовыми
- [ ] Связать тему с MVCC и locking, когда для них появятся статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
