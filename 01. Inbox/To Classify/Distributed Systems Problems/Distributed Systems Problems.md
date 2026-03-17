---
aliases:
  - Problems of Distributed Systems
  - Проблемы распределенных систем
note_type: overview
area: computer-science
domain: distributed-systems
section: distributed-systems-problems
parent:
status: seed
related:
  - "[[Partial Failure]]"
  - "[[Time and Ordering]]"
  - "[[Coordination and Consensus]]"
  - "[[Consistency Under Replication]]"
  - "[[Dual Write]]"
  - "[[Transactional Outbox]]"
tags:
  - consistency
---

# Distributed Systems Problems

## Краткое определение области

Эта обзорная заметка собирает устойчивые классы проблем, которые возникают из-за распределенности: независимых узлов, сетевых задержек, частичных отказов, асинхронности и несовпадения локальных представлений о состоянии системы.

## Что входит в эту тему

- проблемы согласования локального состояния и внешних эффектов;
- проблемы частичных отказов и недостоверности наблюдений;
- проблемы времени, порядка и координации;
- проблемы согласованности реплик и доставки сообщений.

## Как устроена ветка

- Эта заметка служит обзорной рамкой верхнего уровня.
- Под ней должны появляться только реально полезные проблемные кластеры или самостоятельные обзорные подветки.
- `Partial Failure`, `Time and Ordering`, `Coordination and Consensus` и `Consistency Under Replication` уже оправданы как дочерние overview-ветки.
- `Dual Write` уже является оправданной дочерней веткой.

## Рекомендуемый маршрут чтения

1. Начать с этой заметки как с обзорной карты.
2. Затем пройти четыре базовых проблемных кластера: `Partial Failure`, `Time and Ordering`, `Coordination and Consensus`, `Consistency Under Replication`.
3. После этого перейти к `Dual Write` как к частному, но практически важному случаю.
4. Затем читать связанные решения вроде `Transactional Outbox`, `Change Data Capture` и `Distributed Transaction`.

## Соседние overview-ветки

- `[[Partial Failure]]`
- `[[Time and Ordering]]`
- `[[Coordination and Consensus]]`
- `[[Consistency Under Replication]]`

## Что стоит раскрыть дальше

- [ ] Уточнить перечень базовых классов проблем.
- [ ] Проверить, какие из них уже требуют собственных дочерних article.
- [ ] Проверить `related`.
- [ ] Не превращать обзор в пустую таксономию без содержательного наполнения.
