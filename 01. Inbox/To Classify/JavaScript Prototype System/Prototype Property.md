---
aliases:
  - prototype
  - Свойство prototype
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Prototype System]]"
status: seed
related:
  - "[[Internal Prototype Slot]]"
  - "[[Proto Accessor]]"
  - "[[Prototype Chain]]"
tags:
  - javascript
  - objects
---

# Prototype Property

## Краткое определение

Каноническая статья для свойства `prototype`, которое связано с функциями-конструкторами и созданием объектов через `new`.

## Основная идея или механизм

Нужно объяснить, почему `prototype` у функции не тождественен `__proto__` у объекта и не равен самому внутреннему слоту `[[Prototype]]`.

## Границы темы

- Что относится к свойству функций-конструкторов.
- Где тема переходит к lookup по цепочке прототипов или к внутреннему слоту объекта.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Prototype System]]`

Связанные заметки:

- `[[Internal Prototype Slot]]`
- `[[Proto Accessor]]`
- `[[Prototype Chain]]`

## Примеры, случаи или следствия

Добавить пример связи между `Constructor.prototype` и прототипом созданного экземпляра.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
