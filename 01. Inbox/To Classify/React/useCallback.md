---
aliases: []
note_type: article
area: computer-science
domain: frontend-engineering
section: react-hooks
parent: "[[React Hooks]]"
status: seed
related:
  - "[[Rules of Hooks]]"
  - "[[useMemo]]"
  - "[[React.memo]]"
tags: []
---

# useCallback

## Краткое определение

`useCallback` - это hook React для мемоизации функции между рендерами компонента, когда важно сохранять стабильную ссылку на callback.

## Основная идея или механизм

Эта заметка должна объяснять, что `useCallback` относится к стабилизации function reference, а не к мемоизации произвольного значения как `useMemo`.

## Границы темы

- Входит: мемоизация callback-функций и сохранение ссылочной стабильности.
- Не входит: общая тема повторных рендеров компонентов вне связи с callback props.

## Связи с другими заметками

Родительская тема:

`[[React Hooks]]`

Связанные заметки:

- `[[Rules of Hooks]]`
- `[[useMemo]]`
- `[[React.memo]]`

## Примеры, случаи или следствия

Добавить примеры, где `useCallback` полезен для callback props и memoized children, и случаи, где он только усложняет код без реальной пользы.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связь с referential equality
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
