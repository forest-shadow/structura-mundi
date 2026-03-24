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
status: seed
related:
  - "[[Functional Components]]"
  - "[[Component Composition]]"
  - "[[Custom Hooks]]"
  - "[[React.memo]]"
tags: []
---
# Higher-Order Component

## Краткое определение

`Higher-Order Component` — это паттерн React, в котором функция принимает компонент и возвращает новый компонент с расширенным или переиспользуемым поведением.

Базовая форма такого паттерна выглядит как преобразование `Component -> EnhancedComponent`.

## Почему тема находится в ветке React Components

- HOC работает на уровне компонента как абстракции, а не на уровне hook API.
- Он описывает способ повторного использования логики через обёртывание компонентного контракта.
- Поэтому его естественный `parent` — `[[React Components]]`.

## Границы темы

Внутри темы:

- сигнатура HOC и идея обёртки;
- прокидывание `props`;
- композиция нескольких HOC;
- проблемы прозрачности, именования и отладки.

Рядом, но не совпадает с темой:

- `[[Component Composition]]` как более общий принцип;
- `[[Custom Hooks]]` как современная альтернатива повторному использованию логики;
- `[[React.memo]]` как специальная HOC-обёртка React для оптимизации повторных рендеров.

## Связи с другими заметками

Родительская тема:

- `[[React Components]]`

Связанные заметки:

- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Custom Hooks]]`
- `[[React.memo]]`

## Что стоит раскрыть дальше

- [ ] Развести HOC и component composition
- [ ] Добавить сравнение с custom hooks
- [ ] Показать минимальную сигнатуру `Component -> EnhancedComponent`
- [ ] Зафиксировать типичные проблемы HOC: prop collisions, wrapper hell, displayName
