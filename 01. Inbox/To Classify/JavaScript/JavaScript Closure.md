---
aliases:
  - Closure in JavaScript
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[JavaScript Scope Model]]"
status: seed
related:
  - "[[Lexical Scope]]"
  - "[[Scope Chain]]"
tags: []
---

# JavaScript Closure

## Краткое определение

Каноническая статья про closure в JavaScript как способность функции сохранять доступ к внешнему лексическому окружению после завершения выполнения внешнего контекста.

## Основная идея или механизм

Эта заметка должна объяснять, почему closure возникает из сочетания lexical scope и сохранения связанного окружения, и как это влияет на проектирование функций, callbacks и скрытое состояние.

## Границы темы

- Входит: сохранение доступа к внешним переменным, функции-замыкания, практические последствия.
- Не входит: вся тема prototype system, `this` binding или модули как отдельные механизмы.

## Связи с другими заметками

Родительская тема:

`[[JavaScript Scope Model]]`

Связанные заметки:

- `[[Lexical Scope]]`
- `[[Scope Chain]]`

## Примеры, случаи или следствия

Добавить примеры фабрик функций, private state через замыкание и callbacks, удерживающих внешние переменные.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
