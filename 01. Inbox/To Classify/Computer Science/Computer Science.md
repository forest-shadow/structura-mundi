---
aliases:
  - CS
  - Информатика
note_type: overview
area: computer-science
domain:
section:
parent:
status: seed
related:
  - "[[Operating Systems]]"
  - "[[Distributed Systems]]"
  - "[[Software Architecture]]"
  - "[[Programming Languages]]"
  - "[[Computer Architecture]]"
tags: []
---

# Computer Science

## Краткое определение области

`Computer Science` — это area-level overview для корпуса заметок по вычислительным системам, языкам программирования, архитектуре, алгоритмам, сетям, базам данных и инженерным моделям построения программных систем.

## Что входит в эту тему

- `[[Operating Systems]]`
- `[[Distributed Systems]]`
- `[[Software Architecture]]`
- `[[Programming Languages]]`
- `[[Computer Architecture]]`
- `[[Databases]]`
- `[[Networking]]`
- `[[Algorithms]]`
- `[[Frontend Engineering]]`

## Как устроена ветка

- `Computer Science` не должна напрямую собирать product-level заметки вроде `Docker`: между area-root и конкретным термином нужна доменная рамка.
- Для `Docker` такой рамкой здесь выступает `[[Operating Systems]]`, потому что контейнеризация опирается на механизмы изоляции и исполнения, а не только на практики deployment.
- Более узкие кластеры внутри доменов должны появляться как section-level overview, если вокруг них уже есть или ожидается плотный корпус заметок.

## Рекомендуемый маршрут чтения

1. Начать с доменной ветки, соответствующей вопросу.
2. Для темы `Docker` перейти в `[[Operating Systems]]`.
3. Затем читать `[[Containerization]]` и после этого `[[Docker]]`.

## Соседние overview-ветки

- Пока не добавлены.

## Что стоит раскрыть дальше

- [ ] Проверить согласованность domain-root веток внутри `Computer Science`
- [ ] Проверить `related`
