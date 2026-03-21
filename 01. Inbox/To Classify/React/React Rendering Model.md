---
aliases:
  - React Render Cycle
  - React Update Model
note_type: overview
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React]]"
status: seed
related:
  - "[[React Components]]"
  - "[[React Hooks]]"
  - "[[React Render]]"
  - "[[React Reconciliation]]"
  - "[[React State Updates]]"
  - "[[React Component Re-renders]]"
  - "[[React.memo]]"
tags: []
---

# React Rendering Model

## Краткое определение области

Обзорная заметка для того, как React вычисляет обновления интерфейса: как запускается render, как происходит reconciliation, как state updates приводят к повторным рендерам и где в этой картине находится `React.memo`.

## Что входит в эту тему

- `[[React Render]]`
- `[[React Reconciliation]]`
- `[[React State Updates]]`
- `[[React Component Re-renders]]`
- `[[React.memo]]`

## Как устроена ветка

- `React Rendering Model` служит обзорной рамкой для механики обновления UI в React.
- Базовые аспекты модели вынесены в отдельные `article`, чтобы не смешивать process-level и API-level объяснения в одной статье.
- `React.memo` остаётся дочерней статьёй этой ветки, потому что относится к контролю повторных рендеров, а не к hook-кластеру.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `React Rendering Model`.
2. Затем перейти к `[[React Render]]`.
3. После этого читать `[[React Reconciliation]]`.
4. Затем перейти к `[[React State Updates]]`.
5. После этого читать `[[React Component Re-renders]]`.
6. Завершить `[[React.memo]]` как прикладным API-узлом внутри этой модели.

## Соседние overview-ветки

- `[[React Components]]`
- `[[React Hooks]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между rendering model и component model
- [ ] Проверить, нужен ли позже отдельный узел про commit phase
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
