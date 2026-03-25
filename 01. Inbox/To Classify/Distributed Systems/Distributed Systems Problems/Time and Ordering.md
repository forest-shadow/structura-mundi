---
aliases:
  - Время и порядок
note_type: overview
area: computer-science
domain: distributed-systems
section: distributed-systems-problems
parent: "[[Distributed Systems Problems]]"
status: seed
related:
  - "[[Distributed Systems Problems]]"
  - "[[Coordination and Consensus]]"
  - "[[Consistency Under Replication]]"
tags:
  - consistency
---

# Time and Ordering

## Краткое определение области

Обзорная заметка для проблем времени, причинности и порядка событий в распределённых системах, где отсутствуют единые глобальные часы и единая точка наблюдения.

## Что входит в эту тему

- различие между physical time и logical ordering;
- неопределённость порядка событий;
- причинность и happens-before;
- влияние времени и порядка на корректность алгоритмов и протоколов.

## Как устроена ветка

- Ветка нужна как обзорная рамка для проблем, а не только для алгоритмов часов.
- Под ней стоит размещать статьи о causality, event ordering, clock models и соседних проблемах.
- Тема пересекается с `[[Coordination and Consensus]]`, но имеет самостоятельную проблемную оптику.

## Рекомендуемый маршрут чтения

1. Понять, почему в distributed systems нет надёжного глобального порядка по умолчанию.
2. Затем перейти к causality и ordering problems.
3. После этого читать координационные и репликационные следствия.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Coordination and Consensus]]`
- `[[Consistency Under Replication]]`

## Что стоит раскрыть дальше

- [ ] Добавить дочерние заметки о causality и clocks
- [ ] Уточнить границы темы
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
