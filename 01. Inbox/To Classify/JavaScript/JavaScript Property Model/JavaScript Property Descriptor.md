---
aliases:
  - Property Descriptor
  - Дескриптор свойства
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Property Model]]"
status: seed
related:
  - "[[JavaScript Data Property]]"
  - "[[JavaScript Accessor Property]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# JavaScript Property Descriptor

## Краткое определение

`JavaScript Property Descriptor` - это спецификационная и прикладная форма описания свойства объекта через набор атрибутов, определяющих его значение, доступность для записи, getter/setter-поведение, перечисляемость и конфигурируемость.

## Основная идея или механизм

Descriptor позволяет описывать свойство не только как пару `key -> value`, но как структурированную запись. Для data property ключевыми атрибутами являются `value` и `writable`; для accessor property - `get` и `set`; общими атрибутами остаются `enumerable` и `configurable`.

## Границы темы

- Входит: форма descriptor object, distinction между data descriptor и accessor descriptor, связь с `Object.defineProperty`, `Object.getOwnPropertyDescriptor`.
- Не входит: подробная прототипная маршрутизация и наследование свойств; это относится к `[[JavaScript Prototype System]]`.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Property Model]]`

Связанные заметки:

- `[[JavaScript Data Property]]`
- `[[JavaScript Accessor Property]]`
- `[[JavaScript Prototype System]]`

## Примеры, случаи или следствия

Добавить пример descriptor для data property и accessor property, чтобы показать, почему эти две формы не должны смешивать `value/writable` с `get/set`.

## Что стоит раскрыть дальше

- [ ] Уточнить различие data descriptor и accessor descriptor
- [ ] Добавить пример `Object.defineProperty`
- [ ] Добавить пример `Object.getOwnPropertyDescriptor`
- [ ] Проверить `aliases`
