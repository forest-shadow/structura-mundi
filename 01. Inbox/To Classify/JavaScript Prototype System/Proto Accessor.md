---
aliases:
  - __proto__
  - Legacy prototype accessor
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Prototype System]]"
status: seed
related:
  - "[[Internal Prototype Slot]]"
  - "[[Prototype Property]]"
  - "[[Prototype Chain]]"
tags:
  - javascript
  - objects
---

# Proto Accessor

## Краткое определение

Каноническая статья для legacy-accessor `__proto__`, через который можно читать или менять прототип объекта.

## Основная идея или механизм

Нужно показать, что `__proto__` не равен самому `[[Prototype]]`, а является пользовательским accessor-механизмом поверх более глубокой модели.

## Границы темы

- Что относится к публичному API.
- Где тема переходит к внутренней модели спецификации или к `prototype` у функций.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Prototype System]]`

Связанные заметки:

- `[[Internal Prototype Slot]]`
- `[[Prototype Property]]`
- `[[Prototype Chain]]`

## Примеры, случаи или следствия

Добавить пример чтения или изменения прототипа и отметить, почему этот механизм считается legacy.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
