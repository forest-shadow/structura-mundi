---
aliases:
  - Browser Hints
note_type: overview
area: computer-science
domain: web-platform
section: browser-loading-hints
parent: "[[Browser Page Processing]]"
status: seed
related:
  - "[[Browser Rendering]]"
  - "[[Script Loading Attributes]]"
  - "[[Resource Hints]]"
tags:
  - web
  - performance
---

# Browser Loading Hints

## Краткое определение области

Обзорная заметка для механизмов, через которые разработчик подсказывает браузеру, как и когда загружать или исполнять ресурсы страницы.

## Что входит в эту тему

- `[[Script Loading Attributes]]`
- `[[Resource Hints]]`

## Как устроена ветка

- `Browser Loading Hints` служит подветкой внутри более общего узла `Browser Page Processing`.
- Атрибуты `async` и `defer` собраны в отдельную подветку про загрузку скриптов.
- Механизмы `preload`, `prefetch` и `modulepreload` собраны в отдельную подветку resource hints.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Browser Loading Hints`.
2. Затем перейти к `[[Script Loading Attributes]]`.
3. После этого читать `[[Resource Hints]]`.

## Соседние overview-ветки

- `[[Browser Rendering]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между loading hints и broader web performance
- [ ] Проверить, нужен ли позже `preconnect`
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
