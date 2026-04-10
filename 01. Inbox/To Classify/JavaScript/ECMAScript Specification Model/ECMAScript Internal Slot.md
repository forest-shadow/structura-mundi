---
aliases:
  - JavaScript Internal Slot
  - ECMAScript Internal Slots
  - Internal Slot
  - Внутренний слот ECMAScript
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[ECMAScript Specification Model]]"
status: seed
related:
  - "[[ECMAScript Internal Bracket Notation]]"
  - "[[ECMAScript Internal Method]]"
  - "[[JavaScript Prototype Internal Slot]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# ECMAScript Internal Slot

## Краткое определение

`ECMAScript Internal Slot` — это спецификационное внутреннее состояние, ассоциированное с объектом, Symbol, Private Name или иной сущностью стандарта и обозначаемое именем в двойных квадратных скобках.

## Основная идея или механизм

Internal slot описывает состояние, которое нужно стандарту для задания поведения языка, но которое не является обычным свойством объекта, не наследуется и не доступно напрямую из ECMAScript-кода.

Примеры:

```text
[[Prototype]]
[[Extensible]]
[[PrivateElements]]
[[Realm]]
```

## Границы темы

- Входит: общий статус internal slots, отличие от object properties, связь с созданием объектов и спецификационными алгоритмами.
- Не входит: частная прототипная семантика `[[Prototype]]`; она раскрывается в `[[JavaScript Prototype Internal Slot]]`.
- Не входит: поведение internal methods; оно раскрывается в `[[ECMAScript Internal Method]]`.

## Связи с другими заметками

Родительская тема:

`[[ECMAScript Specification Model]]`

Связанные заметки:

- `[[ECMAScript Internal Bracket Notation]]`
- `[[ECMAScript Internal Method]]`
- `[[JavaScript Prototype Internal Slot]]`
- `[[JavaScript Prototype System]]`

## Примеры, случаи или следствия

`[[Prototype]]` является хорошей точкой входа в тему, потому что он часто виден в объяснениях JavaScript, но остается не публичным свойством, а спецификационным внутренним слотом.

## Что стоит раскрыть дальше

- [ ] Уточнить связь с ordinary object creation
- [ ] Добавить отличие от private fields
- [ ] Добавить примеры function-object slots
- [ ] Проверить `related`
