---
aliases:
  - Согласованность при репликации
note_type: overview
area: computer-science
domain: distributed-systems
section: distributed-systems-problems
parent: "[[Distributed Systems Problems]]"
status: seed
related:
  - "[[Distributed Systems Problems]]"
  - "[[Partial Failure]]"
  - "[[Time and Ordering]]"
  - "[[Coordination and Consensus]]"
  - "[[Dual Write]]"
tags:
  - consistency
---

# Consistency Under Replication

## Краткое определение области

Обзорная заметка для проблем согласованности, возникающих тогда, когда одно и то же логическое состояние представлено в нескольких репликах, копиях или локальных представлениях.

## Что входит в эту тему

- расхождение реплик;
- устаревшие чтения и несовпадение локальных представлений;
- компромиссы между latency, availability и consistency;
- связь между replication, delivery и convergence.

## Как устроена ветка

- Ветка фиксирует не конкретную модель consistency, а класс проблем вокруг replicated state.
- Под ней уместны заметки о stale reads, replica lag, convergence и consistency models.
- Тема связана с `[[Dual Write]]`, но не сводится к проблемам внешних эффектов.

## Рекомендуемый маршрут чтения

1. Начать с проблемы расхождения локальных представлений.
2. Затем перейти к consistency models и replication trade-offs.
3. После этого читать частные интеграционные и transactional cases.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Partial Failure]]`
- `[[Time and Ordering]]`
- `[[Coordination and Consensus]]`

## Что стоит раскрыть дальше

- [ ] Добавить первые дочерние заметки о replica lag и consistency models
- [ ] Уточнить связь с message delivery
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
