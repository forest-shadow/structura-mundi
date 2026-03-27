---
aliases:
  - JavaScript Prototypal System
note_type: overview
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript]]"
status: seed
related:
  - "[[JavaScript Prototype Internal Slot]]"
  - "[[Proto Accessor]]"
  - "[[JavaScript prototype Property]]"
  - "[[Prototype Chain]]"
tags: []
---

# JavaScript Prototype System

## Краткое определение области

Обзорная заметка про prototype-based object model в JavaScript и связанные с ней механизмы внутренней связи объектов, доступа к прототипу и разрешения свойств.

## Что входит в эту тему

- `[[JavaScript Prototype Internal Slot]]`
- `[[Proto Accessor]]`
- `[[JavaScript prototype Property]]`
- `[[Prototype Chain]]`

## Как устроена ветка

- `JavaScript Prototype System` служит обзорной рамкой для часто смешиваемых, но нетождественных понятий вокруг прототипов.
- `JavaScript Prototype Internal Slot` описывает внутреннюю спецификационную основу.
- `Proto Accessor` покрывает legacy-пользовательский accessor `__proto__`.
- `JavaScript prototype Property` описывает публичное свойство `prototype` у функций-конструкторов и классов.
- `Prototype Chain` объясняет модель разрешения свойств по цепочке прототипов.

## Рекомендуемый маршрут чтения

1. Начать с `JavaScript Prototype System`.
2. Затем читать `[[JavaScript Prototype Internal Slot]]` и `[[Proto Accessor]]`.
3. После этого перейти к `[[JavaScript prototype Property]]`.
4. Завершить `[[Prototype Chain]]` как моделью lookup и наследования.

## Что стоит раскрыть дальше

- [ ] Проверить, нужна ли позже отдельная статья про `Object.create`
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
