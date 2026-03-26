---
aliases: []
note_type: overview
area: computer-science
domain: web-platform
section: browser-rendering
parent: "[[Browser Page Processing]]"
status: seed
related:
  - "[[Browser Loading Optimization Mechanisms]]"
  - "[[DOM]]"
  - "[[CSSOM]]"
  - "[[Browser Rendering Pipeline]]"
tags:
  - web
  - performance
---

# Browser Rendering

## Краткое определение области

Обзорная заметка про то, как браузер преобразует документ, стили и связанные с ними внутренние структуры в итоговое визуальное представление страницы.

## Что входит в эту тему

- `[[DOM]]`
- `[[CSSOM]]`
- `[[Browser Rendering Pipeline]]`

## Как устроена ветка

- `Browser Rendering` служит подветкой внутри более общего узла `Browser Page Processing`.
- `DOM` и `CSSOM` лучше держать рядом как базовые структуры, а не смешивать их с конкретными стадиями конвейера.
- `Browser Rendering Pipeline` собирает собственно последовательность шагов, ведущих к выводу пикселей на экран.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Browser Rendering`.
2. Затем перейти к `[[DOM]]` и `[[CSSOM]]`.
3. После этого читать `[[Browser Rendering Pipeline]]`.

## Соседние overview-ветки

- `[[Browser Loading Optimization Mechanisms]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между browser rendering и broader web performance
- [ ] Проверить, нужен ли позже отдельный узел про critical rendering path
- [ ] Проверить `related`
