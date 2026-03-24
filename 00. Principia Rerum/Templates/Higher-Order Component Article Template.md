---
aliases:
  - HOC
  - Higher-Order Components
  - React HOC
note_type: article
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React Components]]"
status: draft
related:
  - "[[Functional Components]]"
  - "[[Component Composition]]"
  - "[[Custom Hooks]]"
  - "[[React.memo]]"
tags: []
---

# {{title}}

## Краткое определение

Коротко определить HOC как преобразование `Component -> EnhancedComponent` и зафиксировать, какую именно задачу решает обёртка.

## Почему тема находится в ветке React Components

Объяснить, что HOC работает на уровне компонентного контракта, а не на уровне hook API или общей rendering-модели.

## Формальная схема

```tsx
const EnhancedComponent = withSomething(BaseComponent)
```

Кратко описать:

- что принимает HOC;
- что возвращает HOC;
- как прокидываются `props`.

## Границы темы

- Что относится к HOC как паттерну.
- Чем HOC отличается от `[[Component Composition]]`.
- Чем HOC отличается от `[[Custom Hooks]]`.
- Почему `[[React.memo]]` связан с темой, но не исчерпывает её.

## Практические следствия и ограничения

Указать 1-3 типичных эффекта:

- повторное использование логики;
- обёртывание и усложнение дерева;
- проблемы прозрачности `props`, `displayName` и отладки.

## Связи с другими заметками

Родительская тема:

`[[React Components]]`

Связанные заметки:

- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Custom Hooks]]`
- `[[React.memo]]`

## Что стоит раскрыть дальше

- [ ] Добавить пример простого HOC
- [ ] Добавить сравнение с custom hooks
- [ ] Проверить `aliases`
- [ ] Проверить, не разрастается ли тема до отдельного overview
