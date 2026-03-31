---
aliases:
  - Client Server Architecture
note_type: overview
area: computer-science
domain: networking
section: network-models
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[OSI Model]]"
  - "[[TCP IP Model]]"
  - "[[Client]]"
  - "[[Server]]"
tags: []
---

# Client-Server Model

## Краткое определение области

`Client-Server Model` - это обзорная заметка о базовой модели сетевого взаимодействия, в которой одна сторона инициирует обращения, а другая принимает их и предоставляет сервис.

## Что входит в эту тему

- `[[Client]]`
- `[[Server]]`

## Как устроена ветка

- `Client` фиксирует сторону, которая инициирует обращение и потребляет удаленный сервис.
- `Server` служит более сложным узлом: здесь нужно явно разводить роль, программную реализацию, процесс, хост и endpoint.
- Эта ветка описывает именно логическую модель взаимодействия, а не конкретный стек протоколов или deployment topology.

## Рекомендуемый маршрут чтения

1. Начать с общей схемы `Client-Server Model`.
2. Затем перейти к `[[Client]]` и `[[Server]]`.
3. После этого углубляться в `[[Server Process]]`, если нужен системный и инженерный взгляд.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Смежные model-centric ветки: `[[OSI Model]]`, `[[TCP IP Model]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Load Balancing` и `Service Discovery`
- [ ] Проверить границу между role model и deployment architecture
- [ ] Проверить `related`
