---
aliases:
  - key prop
  - React key
note_type: article
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React Rendering Model]]"
status: seed
related:
  - "[[React Components]]"
  - "[[React Reconciliation]]"
  - "[[React Component Re-renders]]"
tags: []
---

# React Key Prop

## Краткое определение

`key` prop в React - это специальный служебный идентификатор элемента, который помогает алгоритму reconciliation правильно сопоставлять элементы между последовательными рендерами.

## Основная идея или механизм

Эта заметка должна объяснять, что `key` нужен не для передачи данных в компонент, а для сохранения или изменения идентичности элементов в дереве React.

## Границы темы

- Входит: роль `key` в reconciliation и в обновлении списков элементов.
- Не входит: общая тема props как входных данных компонента.

## Связи с другими заметками

Родительская тема:

`[[React Rendering Model]]`

Связанные заметки:

- `[[React Components]]`
- `[[React Component Re-renders]]`

## Примеры, случаи или следствия

Добавить примеры списков, где корректный `key` сохраняет идентичность элементов, и случаев, где индекс массива приводит к ошибкам поведения.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связь с identity и list rendering
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
