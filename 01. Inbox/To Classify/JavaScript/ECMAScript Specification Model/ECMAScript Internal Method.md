---
aliases:
  - JavaScript Internal Method
  - ECMAScript Internal Methods
  - Internal Method
  - Внутренний метод ECMAScript
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[ECMAScript Specification Model]]"
status: seed
related:
  - "[[ECMAScript Internal Bracket Notation]]"
  - "[[ECMAScript Internal Slot]]"
  - "[[ECMAScript Abstract Operation]]"
  - "[[JavaScript Property Model]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# ECMAScript Internal Method

## Краткое определение

`ECMAScript Internal Method` — это спецификационный алгоритм, ассоциированный с объектом и описывающий часть его runtime-поведения; имена таких методов в стандарте записываются в двойных квадратных скобках.

## Основная идея или механизм

Internal methods задают фактическую семантику операций над объектами: получение прототипа, чтение свойства, запись свойства, проверку наличия свойства, определение собственного свойства и другие базовые действия. Они не являются публичными методами JavaScript-объекта и не вызываются напрямую пользовательским кодом.

Примеры:

```text
[[GetPrototypeOf]]
[[SetPrototypeOf]]
[[Get]]
[[Set]]
[[DefineOwnProperty]]
[[Call]]
[[Construct]]
```

## Границы темы

- Входит: общий статус internal methods, отличие от публичных методов объекта, связь с ordinary/exotic object behavior.
- Не входит: внутреннее состояние объекта; оно относится к `[[ECMAScript Internal Slot]]`.
- Не входит: именованные вспомогательные алгоритмы без привязки к target-объекту; они относятся к `[[ECMAScript Abstract Operation]]`.

## Связи с другими заметками

Родительская тема:

`[[ECMAScript Specification Model]]`

Связанные заметки:

- `[[ECMAScript Internal Bracket Notation]]`
- `[[ECMAScript Internal Slot]]`
- `[[ECMAScript Abstract Operation]]`
- `[[JavaScript Property Model]]`
- `[[JavaScript Prototype System]]`

## Примеры, случаи или следствия

`[[Get]]` и `[[Set]]` важны для понимания того, почему чтение и запись свойства в JavaScript не сводятся к простому доступу к таблице ключ-значение.

`[[Call]]` и `[[Construct]]` показывают, почему не всякий function object обязательно является constructor.

## Что стоит раскрыть дальше

- [ ] Уточнить различие ordinary и exotic object internal methods
- [ ] Добавить пример `[[Get]]` в property lookup
- [ ] Добавить пример `[[Call]]` и `[[Construct]]`
- [ ] Проверить `related`
