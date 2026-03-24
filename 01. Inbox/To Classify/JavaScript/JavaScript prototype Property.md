---
aliases:
  - prototype
  - Prototype Property
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Prototype System]]"
status: seed
related:
  - "[[JavaScript Prototype Internal Slot]]"
  - "[[Proto Accessor]]"
  - "[[Prototype Chain]]"
tags: []
---

# JavaScript prototype Property

## Краткое определение

Каноническая статья про публичное свойство `prototype` у функций-конструкторов и классов как объект-шаблон, используемый при создании новых экземпляров в JavaScript.

## Основная идея или механизм

Эта заметка должна объяснять, почему `prototype` не равен ни `[[Prototype]]`, ни `__proto__`, и как через него формируется связь новых объектов с общим объектом-прототипом.

## Границы темы

- Входит: публичное свойство `prototype`, конструкторы, связь с `new`.
- Не входит: внутренняя спецификационная семантика `[[Prototype]]` и legacy-accessor `__proto__` как отдельные темы.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Prototype System]]`

Связанные заметки:

- `[[JavaScript Prototype Internal Slot]]`
- `[[Proto Accessor]]`
- `[[Prototype Chain]]`

## Примеры, случаи или следствия

Добавить примеры, где методы размещаются на `Constructor.prototype`, а экземпляры делят общий prototype object.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
