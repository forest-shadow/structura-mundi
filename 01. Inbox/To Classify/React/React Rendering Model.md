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
  - "[[React Render]]"
  - "[[React Reconciliation]]"
  - "[[React State Updates]]"
  - "[[React Component Re-renders]]"
  - "[[Virtual DOM]]"
tags: []
---

# React Rendering Model

## Краткое определение области

Обзорная заметка про то, как React вычисляет новое представление интерфейса, сопоставляет его с предыдущим и приводит UI к новому состоянию.

## Что входит в эту тему

- `[[React Render]]`
- `[[React Reconciliation]]`
- `[[React State Updates]]`
- `[[React Component Re-renders]]`
- `[[Virtual DOM]]`

## Как устроена ветка

- `React Rendering Model` служит обзорной рамкой для тем про render, reconciliation, state updates и повторные рендеры.
- `Virtual DOM` полезно держать рядом как объясняющую статью про промежуточное представление UI, но не как замену всей rendering-модели.
- Более узкие темы внутри reconciliation стоит выносить только тогда, когда они образуют самостоятельный корпус, а не просто удобный подпункт объяснения.

## Рекомендуемый маршрут чтения

1. Начать с `React Rendering Model`.
2. Затем читать `[[React Render]]` и `[[React Reconciliation]]`.
3. После этого перейти к `[[React State Updates]]` и `[[React Component Re-renders]]`.
4. `[[Virtual DOM]]` использовать как поясняющую статью про внутреннее представление и историческую рамку объяснения.

## Что стоит раскрыть дальше

- [ ] Уточнить границы между render, reconciliation и commit
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
