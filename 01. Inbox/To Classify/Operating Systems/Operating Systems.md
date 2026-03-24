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
  - "[[Computer Science]]"
  - "[[Processes and Threads]]"
  - "[[System Calls]]"
  - "[[File Systems]]"
  - "[[Virtual Memory]]"
tags: []
---

# Operating Systems

## Краткое определение области

`Operating Systems` — это обзорная заметка для ветки про системное программное обеспечение, которое управляет процессами, памятью, доступом к устройствам и базовыми интерфейсами взаимодействия программ с машиной.

## Что входит в эту тему

- `[[Processes and Threads]]`
- `[[System Calls]]`
- `[[File Systems]]`
- `[[Virtual Memory]]`

## Как устроена ветка

- `Processes and Threads` собирает базовую execution-модель ОС.
- `System Calls` описывает интерфейс перехода из user space к сервисам ядра.
- `File Systems` описывает организацию долговременного хранения.
- `Virtual Memory` собирает memory-management подветку, где уже оправдан более глубокий уровень вложенности.

## Рекомендуемый маршрут чтения

1. Начать с `[[Processes and Threads]]`.
2. Затем читать `[[System Calls]]`.
3. После этого перейти к `[[Virtual Memory]]`.
4. В конце смотреть `[[File Systems]]` как отдельный persistent-storage аспект OS.

## Соседние overview-ветки

- Пока не созданы, но позже рядом могут появиться более узкие ветки про distributed systems, runtime systems или computer architecture.

## Что стоит раскрыть дальше

- [ ] Проверить границы между OS-веткой и computer-architecture темами
- [ ] Подтвердить `domain: operating-systems`
- [ ] Проверить, что domain-root overview остается без `section`
- [ ] Проверить `related`
