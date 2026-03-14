---
aliases:
  - Двойная запись
note_type: overview
area: computer-science
domain: distributed-systems
section: dual-write
parent: "[[Distributed Systems Problems]]"
status: seed
related:
  - "[[Distributed Systems Problems]]"
  - "[[Transactional Outbox]]"
  - "[[Change Data Capture]]"
  - "[[Distributed Transaction]]"
tags: []
---

# Dual Write

## Краткое определение области

Dual Write - это проблема, возникающая тогда, когда сервис должен согласованно записать локальное состояние и одновременно зафиксировать внешний эффект, например публикацию события.

## Что входит в эту тему

- способы безопасной публикации после локальной записи;
- способы чтения изменений из локального журнала или таблицы;
- альтернативы, которые пытаются сделать две записи согласованными.

## Как устроена ветка

- На первом уровне достаточно одной обзорной заметки.
- Вложенный `overview` здесь не нужен.
- Дочерние темы лучше держать плоскими `article`.

## Рекомендуемый маршрут чтения

1. Начать с этой заметки.
2. Затем перейти к `Transactional Outbox` как базовому практическому решению.
3. После этого прочитать `Polling Publisher`, `Change Data Capture` и `Distributed Transaction`.

## Соседние overview-ветки

Эта тема уже рассматривается как дочерняя подветка внутри `[[Distributed Systems Problems]]`.

## Что стоит раскрыть дальше

- [ ] Уточнить границы темы.
- [ ] Проверить связь с EDA и consistency concerns.
- [ ] Проверить `related`.
- [ ] Не создавать лишний промежуточный уровень.
