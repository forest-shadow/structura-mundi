---
aliases:
  - Контейнеризация
  - Software Containers
note_type: overview
area: computer-science
domain: operating-systems
section: containerization
parent: "[[Operating Systems]]"
status: seed
related:
  - "[[Operating Systems]]"
  - "[[Docker]]"
tags: []
---

# Containerization

## Краткое определение области

`Containerization` — это section-level overview внутри `operating-systems`, которая собирает заметки о контейнерной изоляции процессов, упаковке приложений в образы и механизмах исполнения контейнеров поверх ядра ОС.

## Что входит в эту тему

- `[[Docker]]`

## Как устроена ветка

- Этот узел нужен, чтобы держать `Docker` не как одиночный продуктовый термин, а как часть более широкой темы про контейнеры.
- Внутри этой ветки естественно могут появиться sibling-заметки про container images, container runtimes, `Linux namespaces`, `cgroups`, OCI и контейнерные сетевые механизмы.
- Пока не стоит заранее дробить ветку на дополнительные sub-overview, если корпус ещё не вырос.

## Рекомендуемый маршрут чтения

1. Начать с `[[Operating Systems]]`.
2. Затем перейти к `[[Containerization]]` как к общей рамке.
3. После этого читать `[[Docker]]` и соседние статьи по мере их появления.

## Соседние overview-ветки

- Родительская рамка: `[[Operating Systems]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Docker` нужны `Container Image` и `Container Runtime`
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
