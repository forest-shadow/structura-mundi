---
aliases:
  - OS Virtual Memory
  - Operating System Virtual Memory
note_type: overview
area: computer-science
domain: operating-systems
section: memory-management
parent: "[[Operating Systems]]"
status: seed
related:
  - "[[Operating Systems]]"
  - "[[Virtual Address Space]]"
  - "[[Paging]]"
tags: []
---

# Virtual Memory

## Краткое определение области

`Virtual Memory` — это обзорная заметка про механизм операционной системы, который дает процессам абстракцию собственного адресного пространства и связывает виртуальные адреса с физической памятью и вторичным хранением.

## Что входит в эту тему

- `[[Virtual Address Space]]`
- `[[Paging]]`

## Как устроена ветка

- `Virtual Memory` теперь является дочерним `sub-overview` внутри `[[Operating Systems]]`.
- `Virtual Address Space` фиксирует, какую именно абстракцию видит процесс.
- `Paging` собирает под одной рамкой механизм разбиения памяти на страницы, структуру отображения и поведение системы при промахах по отображению.
- Более детальные темы про translation cache и faults живут внутри `Paging`, а не напрямую под корнем.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Virtual Memory`.
2. Затем перейти к `[[Virtual Address Space]]`.
3. После этого читать `[[Paging]]`.
4. Внутри `Paging` идти к `[[Page Table]]`, `[[TLB]]` и `[[Page Fault]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Operating Systems]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между virtual memory и общей memory management темой
- [ ] Подтвердить `domain: operating-systems`
- [ ] Подтвердить `section: memory-management`
- [ ] Проверить `related`
