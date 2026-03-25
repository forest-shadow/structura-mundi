---
aliases:
  - Частичный отказ
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

# Partial Failure

## Краткое определение области

Обзорная заметка для проблем, возникающих из-за того, что в распределённой системе часть компонентов может отказать, зависнуть или стать недоступной, пока остальные продолжают работать.

## Что входит в эту тему

- неразличимость отказа и задержки;
- локальная неполнота наблюдения;
- расхождение решений между узлами;
- деградация системы при частичной недоступности.

## Как устроена ветка

- Это обзорный узел для устойчивого кластера проблем, а не для одного частного механизма.
- Под ним стоит заводить только реальные problem-centered статьи и подветки.
- Тема тесно связана с `[[Coordination and Consensus]]`, но не сводится к ней.

## Рекомендуемый маршрут чтения

1. Начать с понимания partial failure как фундаментального свойства distributed systems.
2. Затем перейти к темам координации и репликации.
3. После этого читать частные проблемные сценарии и компромиссы.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Coordination and Consensus]]`
- `[[Consistency Under Replication]]`

## Что стоит раскрыть дальше

- [ ] Добавить первые дочерние problem notes
- [ ] Уточнить границы между partial failure и fault tolerance
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
