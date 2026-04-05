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
  - "[[Software Development]]"
tags: []
---

# Computer Science

## Краткое определение области

`Computer Science` — это area-level overview для корпуса заметок по вычислительным системам, языкам программирования, архитектуре, алгоритмам, сетям, инженерным инструментам разработки и моделям построения программных систем.

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
- `[[Software Development]]`

## Как устроена ветка

- `Computer Science` не должна напрямую собирать product-level заметки вроде `Docker` или `Vim`: между area-root и конкретным термином нужна доменная рамка.
- Для `Docker` такой рамкой здесь выступает `[[Operating Systems]]`, потому что контейнеризация опирается на механизмы изоляции и исполнения, а не только на практики deployment.
- Для `Vim` такой рамкой выступает `[[Software Development]]`, потому что речь идет не о языке программирования и не об архитектурной теории, а об инструментах и практиках разработки.
- Более узкие кластеры внутри доменов должны появляться как section-level overview, если вокруг них уже есть или ожидается плотный корпус заметок.

## Рекомендуемый маршрут чтения

1. Начать с доменной ветки, соответствующей вопросу.
2. Для темы `Docker` перейти в `[[Operating Systems]]`.
3. Для темы `Vim` перейти в `[[Software Development]]`, затем в `[[Vim]]`.
4. После этого уже входить в соответствующие sub-overview и article-заметки.

## Соседние overview-ветки

- Пока не добавлены.

## Что стоит раскрыть дальше

- [ ] Проверить согласованность domain-root веток внутри `Computer Science`
- [ ] Проверить границу между `Software Development` и `Software Architecture`
- [ ] Проверить `related`
