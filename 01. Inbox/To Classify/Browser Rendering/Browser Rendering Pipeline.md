---
aliases:
  - Rendering Pipeline
note_type: overview
area: computer-science
domain: web-platform
section: browser-rendering-pipeline
parent: "[[Browser Rendering]]"
status: seed
related:
  - "[[Render Tree]]"
  - "[[Layout]]"
  - "[[Paint]]"
  - "[[Compositing]]"
tags:
  - web
  - performance
---

# Browser Rendering Pipeline

## Краткое определение области

Обзорная заметка для последовательности стадий, через которые браузер превращает входные структуры страницы в итоговое визуальное изображение на экране.

## Что входит в эту тему

- `[[Render Tree]]`
- `[[Layout]]`
- `[[Paint]]`
- `[[Compositing]]`

## Как устроена ветка

- `Browser Rendering Pipeline` служит обзорной рамкой именно для стадий конвейера, а не для всех browser APIs сразу.
- `Render Tree` полезно держать отдельно как переходную структуру между `DOM`, `CSSOM` и визуальными стадиями.
- `Layout`, `Paint` и `Compositing` лучше держать отдельными `article`, потому что это разные по смыслу и стоимости этапы.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Browser Rendering Pipeline`.
2. Затем читать `[[Render Tree]]`.
3. После этого перейти к `[[Layout]]`, `[[Paint]]` и `[[Compositing]]`.

## Соседние overview-ветки

- `[[Browser Rendering]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, где в pipeline удобнее раскрывать style calculation
- [ ] Проверить, нужна ли позже отдельная статья про reflow и repaint
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
