---
aliases:
  - OS
  - Operating System
note_type: overview
area: computer-science
domain: operating-systems
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Processes and Threads]]"
  - "[[System Calls]]"
  - "[[File Systems]]"
  - "[[Virtual Memory]]"
  - "[[Containerization]]"
tags: []
---

# Operating Systems

## Краткое определение области

`Operating Systems` — это domain-root overview внутри `computer-science`, которая собирает заметки о механизмах выполнения, изоляции, управления памятью, файловых интерфейсах и системных абстракциях, через которые программный код взаимодействует с машиной.

## Что входит в эту тему

- `[[Processes and Threads]]`
- `[[System Calls]]`
- `[[File Systems]]`
- `[[Virtual Memory]]`
- `[[Containerization]]`

## Как устроена ветка

- `Processes and Threads`, `System Calls`, `File Systems` и `Virtual Memory` описывают базовые механизмы ОС.
- `Containerization` оправдана как отдельный локальный overview, потому что тема естественно собирает рядом `Docker`, container runtime, образы, Linux namespaces, cgroups и OCI-related понятия.
- `Docker` не стоит подвешивать напрямую под `Operating Systems`, если ожидается дальнейший рост ветки про контейнеры как самостоятельный кластер.

## Рекомендуемый маршрут чтения

1. Начать с `[[Processes and Threads]]` и `[[System Calls]]` как системного фундамента.
2. Затем перейти к `[[Virtual Memory]]` и `[[File Systems]]`.
3. Для контейнерной ветки читать `[[Containerization]]`, а затем `[[Docker]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить, что `Containerization` получает собственный `section`
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
