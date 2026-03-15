---
aliases:
  - Context hook
note_type: article
area: computer-science
domain: frontend-engineering
section: react-hooks
parent: "[[React Hooks]]"
status: seed
related:
  - "[[useReducer]]"
  - "[[Custom Hooks]]"
tags: []
---

# useContext

## Краткое определение

`useContext` - это hook, который позволяет компоненту читать значение React context без ручного wiring через props на каждом уровне дерева.

## Основная идея или механизм

Нужно раскрыть, как `useContext` работает с provider-деревом и какие ограничения или риски появляются при слишком широком использовании context.

## Границы темы

- Что относится к `useContext`.
- Чем context отличается от локального state и внешнего store.

## Связи с другими заметками

Родительская тема:

`[[React Hooks]]`

Связанные заметки:

- `[[useReducer]]`
- `[[Custom Hooks]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария чтения theme, auth или shared configuration.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
