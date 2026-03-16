---
aliases:
  - "[[Prototype]]"
  - Внутренний слот прототипа
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Prototype System]]"
status: seed
related:
  - "[[Proto Accessor]]"
  - "[[Prototype Property]]"
  - "[[Prototype Chain]]"
tags:
  - javascript
  - objects
---

# Internal Prototype Slot

## Краткое определение

Каноническая статья для внутреннего механизма, через который объект в JavaScript связан со своим прототипом.

## Основная идея или механизм

Нужно объяснить, что `[[Prototype]]` является внутренним слотом спецификации, а не обычным публичным свойством объекта.

## Границы темы

- Что относится именно к внутренней модели спецификации.
- Где тема переходит в пользовательские механизмы доступа вроде `__proto__`.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Prototype System]]`

Связанные заметки:

- `[[Proto Accessor]]`
- `[[Prototype Property]]`
- `[[Prototype Chain]]`

## Примеры, случаи или следствия

Добавить короткий пример того, как наличие внутреннего прототипа влияет на lookup свойств.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
