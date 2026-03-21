---
aliases:
  - React Memo
note_type: article
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React Rendering Model]]"
status: seed
related:
  - "[[Functional Components]]"
  - "[[Props in React]]"
  - "[[React Component Re-renders]]"
  - "[[useMemo]]"
tags: []
---





# React.memo

## Краткое определение

`React.memo` - это API для мемоизации функционального компонента, которое позволяет React пропускать повторный рендер, если входные props не изменились по ожидаемому правилу сравнения.

## Основная идея или механизм

Эта заметка должна объяснять, что `React.memo` относится к модели повторных рендеров компонентов, а не к кешированию произвольных вычислений внутри компонента.

## Границы темы

- Входит: мемоизация компонента на уровне props и повторных рендеров.
- Не входит: мемоизация значений через `useMemo` и хранение ссылок через `useRef`.

## Связи с другими заметками

Родительская тема:

`[[React Rendering Model]]`

Связанные заметки:

- `[[Functional Components]]`
- `[[Props in React]]`
- `[[React Component Re-renders]]`
- `[[useMemo]]`

## Примеры, случаи или следствия

Добавить примеры, где `React.memo` уменьшает лишние рендеры дочерних компонентов, и случаи, где он не даёт пользы или усложняет модель.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связь с shallow comparison props
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
