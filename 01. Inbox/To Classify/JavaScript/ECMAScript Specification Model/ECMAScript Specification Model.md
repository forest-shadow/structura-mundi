---
aliases:
  - JavaScript Specification Model
  - ECMAScript Spec Model
note_type: overview
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript]]"
status: seed
related:
  - "[[ECMAScript Internal Bracket Notation]]"
  - "[[ECMAScript Internal Slot]]"
  - "[[ECMAScript Internal Method]]"
  - "[[ECMAScript Abstract Operation]]"
  - "[[JavaScript Prototype System]]"
  - "[[JavaScript Property Model]]"
tags: []
---

# ECMAScript Specification Model

## Краткое определение области

`ECMAScript Specification Model` — обзорная заметка про формальный язык спецификации ECMAScript: как стандарт обозначает внутреннее состояние, внутренние методы, абстрактные операции и служебные структуры, которые не являются прямым пользовательским синтаксисом JavaScript.

## Что входит в эту тему

- `[[ECMAScript Internal Bracket Notation]]`
- `[[ECMAScript Internal Slot]]`
- `[[ECMAScript Internal Method]]`
- `[[ECMAScript Abstract Operation]]`

## Как устроена ветка

- `ECMAScript Internal Bracket Notation` объясняет, как читать имена вида `[[Prototype]]`, `[[Get]]`, `[[Value]]` и `[[Type]]`.
- `ECMAScript Internal Slot` описывает внутреннее спецификационное состояние, связанное с объектами и другими значениями спецификации.
- `ECMAScript Internal Method` описывает алгоритмическое поведение объектов, которое стандарт использует для задания runtime-семантики.
- `ECMAScript Abstract Operation` описывает именованные алгоритмы спецификации, которые используются для формализации шагов выполнения, но не являются публичными функциями языка.

## Рекомендуемый маршрут чтения

1. Начать с `ECMAScript Specification Model`.
2. Затем перейти к `[[ECMAScript Internal Bracket Notation]]`.
3. После этого читать `[[ECMAScript Internal Slot]]` и `[[ECMAScript Internal Method]]` как две соседние категории.
4. Для понимания алгоритмического слоя перейти к `[[ECMAScript Abstract Operation]]`.
5. Для прикладной связи с объектной моделью вернуться к `[[JavaScript Prototype System]]` и `[[JavaScript Property Model]]`.

## Соседние overview-ветки

- `[[JavaScript]]`
- `[[JavaScript Prototype System]]`
- `[[JavaScript Property Model]]`

## Что стоит раскрыть дальше

- [ ] Уточнить различие между notation, internal slot и internal method
- [ ] Добавить примеры из `[[JavaScript Prototype Internal Slot]]`
- [ ] Проверить, нужен ли отдельный article про specification records
- [ ] Проверить `related`
