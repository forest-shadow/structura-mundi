---
aliases: []
note_type: overview
area: computer-science
domain: web-platform
section: resource-hints
parent: "[[Browser Loading Optimization Mechanisms]]"
status: seed
related:
  - "[[DNS Prefetch]]"
  - "[[Preconnect]]"
  - "[[Preload]]"
  - "[[Prefetch]]"
  - "[[Modulepreload]]"
  - "[[Fetch Priority]]"
tags:
  - web
  - performance
---

# Resource Hints

## Краткое определение области

Обзорная заметка для канонического семейства hints, которыми разработчик подсказывает браузеру, какие соединения стоит подготовить заранее и какие ресурсы стоит обнаружить или загрузить до момента естественного запроса.

## Что входит в эту тему

- `[[DNS Prefetch]]`
- `[[Preconnect]]`
- `[[Preload]]`
- `[[Prefetch]]`
- `[[Modulepreload]]`

## Как устроена ветка

- `DNS Prefetch` и `Preconnect` относятся к прогреву соединений.
- `Preload` и `Modulepreload` относятся к раннему обнаружению и приоритетной загрузке ресурсов текущей страницы.
- `Prefetch` относится к вероятному будущему использованию и потому живёт в другой части смыслового пространства, чем `preload`.
- `Fetch Priority` стоит рядом как соседний механизм, но не входит в семейство `Resource Hints`.

## Что не входит в эту тему

- Атрибуты `async` и `defer`, потому что они относятся к поведению `<script>`, а не к link-based hints.
- `Fetch Priority`, потому что это отдельный механизм про приоритет уже обнаруженных загрузок.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Resource Hints`.
2. Затем читать `[[DNS Prefetch]]` и `[[Preconnect]]`.
3. После этого перейти к `[[Preload]]`.
4. Затем читать `[[Prefetch]]`.
5. После этого перейти к `[[Modulepreload]]`.

## Соседние overview-ветки

- `[[Script Loading and Execution Attributes]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, когда стоит отдельно добавить исторический `prerender`
- [ ] Проверить, нужен ли позже отдельный узел про `Speculation Rules API`
- [ ] Проверить `related`
