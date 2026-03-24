---
aliases:
  - "[[Prototype]]"
  - Internal Prototype Slot
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Prototype System]]"
status: seed
related:
  - "[[Proto Accessor]]"
  - "[[JavaScript prototype Property]]"
  - "[[Prototype Chain]]"
tags: []
---

# JavaScript Prototype Internal Slot

## Краткое определение

Каноническая статья про внутренний слот `[[Prototype]]` как спецификационный механизм связи объекта с его прототипом в JavaScript.

## Основная идея или механизм

Эта заметка должна объяснять, что `[[Prototype]]` не является обычным публичным свойством объекта, а выступает внутренней основой prototype-based object model и lookup по цепочке прототипов.

## Границы темы

- Входит: внутренний слот `[[Prototype]]`, его роль в объектной модели и связи с lookup свойств.
- Не входит: вся тема legacy-accessor `__proto__` или публичного свойства `prototype` у функций как самостоятельных механизмов.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Prototype System]]`

Связанные заметки:

- `[[Proto Accessor]]`
- `[[JavaScript prototype Property]]`
- `[[Prototype Chain]]`

## Примеры, случаи или следствия

Добавить примеры, показывающие различие между внутренним `[[Prototype]]`, legacy-accessor `__proto__` и публичным свойством `prototype`.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
