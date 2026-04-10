---
aliases:
  - Data Property
  - Свойство-данное
  - Свойство данных
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Property Model]]"
status: seed
related:
  - "[[JavaScript Property Descriptor]]"
  - "[[JavaScript Accessor Property]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# JavaScript Data Property

## Краткое определение

`JavaScript Data Property` - это свойство объекта, которое непосредственно хранит значение и описывается через data descriptor с атрибутами `value` и `writable`.

## Основная идея или механизм

Data property соответствует привычной модели свойства как хранимого значения по ключу. Чтение возвращает сохраненное значение, а запись пытается изменить это значение или создать новое собственное свойство в зависимости от контекста, атрибутов и прототипной цепочки.

## Границы темы

- Входит: `value`, `writable`, отличие от accessor property, базовое поведение при чтении и записи.
- Не входит: getter/setter-семантика; она относится к `[[JavaScript Accessor Property]]`.
- Не входит: полный алгоритм поиска свойства по прототипной цепочке; он относится к `[[JavaScript Prototype System]]`.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Property Model]]`

Связанные заметки:

- `[[JavaScript Property Descriptor]]`
- `[[JavaScript Accessor Property]]`
- `[[JavaScript Prototype System]]`

## Примеры, случаи или следствия

Добавить пример обычного свойства объекта и пример `Object.defineProperty` с `writable: false`.

## Что стоит раскрыть дальше

- [ ] Уточнить связь с own property
- [ ] Добавить пример writable/non-writable behavior
- [ ] Добавить контраст с accessor property
- [ ] Проверить `related`
