---
aliases: []
note_type: article
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React Rendering Model]]"
status: seed
related:
  - "[[React Render]]"
  - "[[React Component Re-renders]]"
  - "[[React Key Prop]]"
tags: []
---

# React Reconciliation

## Краткое определение

Каноническая статья про reconciliation в React как механизм сопоставления нового и предыдущего представления UI для вычисления необходимых изменений.

## Основная идея или механизм

Эта заметка должна объяснять, как React сравнивает деревья элементов и почему reconciliation нужно отличать и от render, и от фактического применения изменений к интерфейсу.

На текущем этапе `Principia Rerum` здесь важно не переусложнять ветку. Темы вроде identity элементов, list diffing, preserving/resetting state и remount vs update пока лучше раскрывать как разделы внутри этой статьи, а не выносить в отдельные заметки без достаточного корпуса.

## Границы темы

- Входит: reconciliation как механизм сравнения и выбора обновлений.
- Не входит: общая тема состояния компонентов вне связи с обновлением дерева.

## Что пока не нужно выносить в отдельные статьи

- identity элементов в дереве React;
- list diffing как частный аспект reconciliation;
- preserving and resetting state;
- remount vs update.

Эти темы уже естественно входят в объяснение reconciliation, но пока не образуют отдельную устойчивую подветку.

## Связи с другими заметками

Родительская тема:

`[[React Rendering Model]]`

Связанные заметки:

- `[[React Render]]`
- `[[React Component Re-renders]]`
- `[[React Key Prop]]`

## Примеры, случаи или следствия

Добавить примеры, где различие между render и reconciliation помогает понять обновление компонентов, и место `React Key Prop` в этой логике.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
