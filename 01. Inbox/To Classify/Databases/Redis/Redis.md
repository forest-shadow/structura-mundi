---
aliases: []
note_type: overview
area: computer-science
domain: databases
section: redis
parent: "[[Databases]]"
status: seed
related:
  - "[[Databases]]"
  - "[[Redis Sorted Set]]"
  - "[[Distributed Cache]]"
tags: []
---

# Redis

## Краткое определение области

`Redis` — это section-level overview внутри `databases` для заметок о Redis как in-memory data structure store: его модели данных, типах структур, operational behavior и типичных сценариях использования.

## Что входит в эту тему

- `[[Redis Sorted Set]]`

## Как устроена ветка

- `Redis` оправдан как отдельный overview-узел, потому что рядом с ним естественно собираются темы про data types, expiration, persistence, replication и прикладные trade-offs.
- На текущем этапе не нужно вводить дополнительный уровень вроде `Redis Data Types`, пока внутри ветки нет нескольких sibling-заметок.
- Поперечная связь с `[[Distributed Cache]]` важна, но она не заменяет database-оптику: Redis здесь рассматривается не только как кэш, но и как самостоятельная модель хранения и доступа к данным.

## Рекомендуемый маршрут чтения

1. Начать с `[[Redis Sorted Set]]` как первого конкретного Redis-специфичного примитива.
2. Затем по мере роста ветки добавлять рядом другие структуры данных и operational topics.

## Соседние overview-ветки

- Родительская рамка: `[[Databases]]`
- Поперечная инфраструктурная связь: `[[Distributed Cache]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про другие Redis data types
- [ ] Решить, когда нужны notes про expiration, persistence и replication
- [ ] Проверить `related`
