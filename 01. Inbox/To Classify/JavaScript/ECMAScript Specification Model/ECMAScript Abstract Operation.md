---
aliases:
  - JavaScript Abstract Operation
  - ECMAScript Abstract Operations
  - Abstract Operation
  - Абстрактная операция ECMAScript
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[ECMAScript Specification Model]]"
status: seed
related:
  - "[[ECMAScript Internal Bracket Notation]]"
  - "[[ECMAScript Internal Slot]]"
  - "[[ECMAScript Internal Method]]"
  - "[[JavaScript Prototype Internal Slot]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# ECMAScript Abstract Operation

## Краткое определение

`ECMAScript Abstract Operation` — это именованный алгоритм спецификации ECMAScript, используемый стандартом для формального описания шагов вычисления, создания значений и проверки инвариантов языка.

## Основная идея или механизм

Abstract operation не является публичной функцией JavaScript. Это служебный алгоритм спецификации: он может принимать аргументы, возвращать normal/abrupt completion, обращаться к internal slots и internal methods, а также вызываться из других алгоритмов стандарта.

Примеры:

```text
OrdinaryObjectCreate
OrdinaryCreateFromConstructor
GetPrototypeFromConstructor
RequireInternalSlot
```

## Границы темы

- Входит: общий статус abstract operations, отличие от пользовательского API и internal methods, роль в чтении спецификационных алгоритмов.
- Не входит: конкретный полный разбор каждого алгоритма; такие разборы стоит выносить отдельно только при устойчивой необходимости.
- Не входит: сами internal slots и internal methods как категории; они раскрываются в соседних заметках.

## Связи с другими заметками

Родительская тема:

`[[ECMAScript Specification Model]]`

Связанные заметки:

- `[[ECMAScript Internal Bracket Notation]]`
- `[[ECMAScript Internal Slot]]`
- `[[ECMAScript Internal Method]]`
- `[[JavaScript Prototype Internal Slot]]`
- `[[JavaScript Prototype System]]`

## Примеры, случаи или следствия

`OrdinaryObjectCreate` помогает понять, как стандарт описывает создание ordinary object и установку internal slots вроде `[[Prototype]]`.

`GetPrototypeFromConstructor` показывает связь между публичным свойством конструктора `prototype` и внутренним слотом создаваемого объекта.

## Что стоит раскрыть дальше

- [ ] Уточнить отличие abstract operation от internal method
- [ ] Добавить пример `OrdinaryObjectCreate`
- [ ] Добавить пример `RequireInternalSlot`
- [ ] Проверить `aliases`
