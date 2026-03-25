---
aliases:
  - Координация и консенсус
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
  - "[[Consistency Under Replication]]"
tags:
  - consistency
---

# Coordination and Consensus

## Краткое определение области

Обзорная заметка для проблем, возникающих тогда, когда нескольким узлам нужно прийти к совместимому решению или согласованному порядку действий в условиях отказов, задержек и неполной информации.

## Что входит в эту тему

- необходимость координации между узлами;
- достижение общего решения;
- компромиссы между прогрессом, безопасностью и доступностью;
- роль consensus как частного, но центрального класса задач.

## Как устроена ветка

- Это обзорная problem-centered ветка, а не каталог конкретных протоколов.
- Под ней могут появляться как статьи о coordination problems, так и отдельные заметки о consensus families.
- Ветка стоит рядом с `[[Partial Failure]]` и `[[Time and Ordering]]`, потому что опирается на обе эти проблемы.

## Рекомендуемый маршрут чтения

1. Начать с причин, по которым координация вообще становится трудной.
2. Затем перейти к consensus как специальному классу задач.
3. После этого связывать тему с репликацией и отказами.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Partial Failure]]`
- `[[Time and Ordering]]`
- `[[Consistency Under Replication]]`

## Что стоит раскрыть дальше

- [ ] Добавить первые дочерние заметки о coordination problems
- [ ] Решить, когда нужна отдельная ветка для consensus protocols
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
