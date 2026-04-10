---
aliases:
  - Accessor Property
  - Javascript Accessor Property
  - Свойство-аксессор
  - Аксессорное свойство
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Property Model]]"
status: seed
related:
  - "[[JavaScript Property Descriptor]]"
  - "[[JavaScript Data Property]]"
  - "[[Proto Accessor]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# JavaScript Accessor Property

## Краткое определение

`JavaScript Accessor Property` - это свойство объекта, которое не хранит значение напрямую, а описывает операции чтения и записи через getter и setter функции.

## Основная идея или механизм

Accessor property задается accessor descriptor: вместо атрибутов `value` и `writable` оно использует `get` и `set`, а также общие атрибуты `enumerable` и `configurable`. При чтении свойства вызывается getter, при записи - setter; если соответствующая функция отсутствует, поведение отличается от обычного data property.

## Границы темы

- Входит: getter/setter-семантика, отличие от data property, связь с accessor descriptor.
- Входит как важный пример: `[[Proto Accessor]]`, потому что `__proto__` является конкретным legacy accessor property на `Object.prototype`.
- Не входит: вся прототипная модель JavaScript; она раскрывается в `[[JavaScript Prototype System]]`.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Property Model]]`

Связанные заметки:

- `[[JavaScript Property Descriptor]]`
- `[[JavaScript Data Property]]`
- `[[Proto Accessor]]`
- `[[JavaScript Prototype System]]`

## Примеры, случаи или следствия

Добавить пример с `get name()` / `set name(value)` в литерале объекта и пример с `Object.defineProperty`, чтобы показать descriptor-level форму accessor property.

## Что стоит раскрыть дальше

- [ ] Уточнить поведение при отсутствующем setter
- [ ] Добавить пример object literal getter/setter
- [ ] Добавить пример `Object.defineProperty`
- [ ] Связать с `[[Proto Accessor]]` как частным историческим случаем
