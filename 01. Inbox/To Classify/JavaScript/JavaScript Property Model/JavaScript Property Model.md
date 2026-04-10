---
aliases:
  - JavaScript Object Property Model
  - JavaScript Properties
note_type: overview
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript]]"
status: seed
related:
  - "[[JavaScript Property Descriptor]]"
  - "[[JavaScript Data Property]]"
  - "[[JavaScript Accessor Property]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# JavaScript Property Model

## Краткое определение области

Обзорная заметка про то, как JavaScript представляет свойства объектов: через ключи, атрибуты, дескрипторы и различие между data properties и accessor properties.

## Что входит в эту тему

- `[[JavaScript Property Descriptor]]`
- `[[JavaScript Data Property]]`
- `[[JavaScript Accessor Property]]`

## Как устроена ветка

- `JavaScript Property Model` служит обзорной рамкой для базовой семантики свойств объекта.
- `JavaScript Property Descriptor` объясняет форму описания свойства и связывает descriptor-level представление с API вроде `Object.defineProperty`.
- `JavaScript Data Property` описывает свойство, которое хранит значение.
- `JavaScript Accessor Property` описывает свойство, чье чтение и запись делегируются getter/setter-функциям.

## Рекомендуемый маршрут чтения

1. Начать с `JavaScript Property Model`.
2. Затем перейти к `[[JavaScript Property Descriptor]]`.
3. После этого читать `[[JavaScript Data Property]]` и `[[JavaScript Accessor Property]]` как две соседние разновидности свойств.
4. Для связи с наследованием перейти к `[[JavaScript Prototype System]]` и `[[Proto Accessor]]`.

## Соседние overview-ветки

- `[[JavaScript]]`
- `[[JavaScript Prototype System]]`
- `[[JavaScript Scope Model]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между property model и prototype lookup
- [ ] Добавить примеры `Object.defineProperty`
- [ ] Проверить, нужен ли отдельный article `JavaScript Own Property`
- [ ] Проверить `related`
