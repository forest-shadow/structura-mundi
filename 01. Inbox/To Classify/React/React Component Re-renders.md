---
aliases:
  - React Re-renders
note_type: article
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React Rendering Model]]"
status: seed
related:
  - "[[React State Updates]]"
  - "[[React Reconciliation]]"
  - "[[React.memo]]"
tags: []
---

# React Component Re-renders

## Краткое определение

Каноническая статья про повторные рендеры компонентов в React как наблюдаемое следствие state changes, props changes и решений самой rendering model.

## Основная идея или механизм

Эта заметка должна объяснять, почему компонент может быть пересчитан повторно, как это связано с деревом компонентов и где в эту картину входит `React.memo`.

## Границы темы

- Входит: причины и последствия повторных рендеров компонентов.
- Не входит: низкоуровневая детализация всех оптимизаций вне устойчивых основных механизмов.

## Связи с другими заметками

Родительская тема:

`[[React Rendering Model]]`

Связанные заметки:

- `[[React State Updates]]`
- `[[React Reconciliation]]`
- `[[React.memo]]`

## Примеры, случаи или следствия

Добавить сценарии, где ререндер родителя тянет за собой дочерние компоненты, и случаи, где `React.memo` помогает ограничить это поведение.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
