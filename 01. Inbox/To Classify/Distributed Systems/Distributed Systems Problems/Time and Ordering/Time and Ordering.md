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
  - "[[Time and Ordering]]"
  - "[[Distributed Systems Problems]]"
  - "[[Clock Synchronization]]"
  - "[[Coordination and Consensus]]"
tags:
  - consistency
---

# Time and Ordering

## Краткое определение области

Обзорная заметка для проблем времени, причинности и порядка событий в распределённых системах, где отсутствуют единые глобальные часы и единая точка наблюдения.

## Что входит в эту тему

- различие между physical time и logical ordering;
- использование `UTC` как внешней reference-scale для wall-clock timestamps;
- синхронизация локальных часов между узлами;
- неопределённость порядка событий;
- причинность и happens-before;
- влияние времени и порядка на корректность алгоритмов и протоколов.

## Как устроена ветка

- Ветка нужна как обзорная рамка для проблем, а не только для алгоритмов часов.
- `UTC` здесь играет роль общей точки отсчёта для физических часов и timestamp-based координации.
- `Clock Synchronization` удерживает operational-слой: как узлы приближают свои локальные часы к общей временной шкале.
- Под ней стоит размещать статьи о causality, event ordering, clock models и соседних проблемах.
- Тема пересекается с `[[Coordination and Consensus]]`, но имеет самостоятельную проблемную оптику.

## Рекомендуемый маршрут чтения

1. Понять, почему в distributed systems нет надёжного глобального порядка по умолчанию.
2. Затем посмотреть, зачем нужен внешний reference-time через `[[UTC]]` и почему этого всё равно недостаточно без `[[Clock Synchronization]]`.
3. После этого перейти к causality, ordering problems и логическим clock-моделям.
4. Затем читать координационные и репликационные следствия.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Coordination and Consensus]]`
- `[[Consistency Under Replication]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны отдельные заметки про logical clocks и vector clocks
- [ ] Решить, когда `Clock Synchronization` потребует отдельную статью про NTP
- [ ] Уточнить границы темы
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
