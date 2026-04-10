---
aliases:
  - JavaScript Internal Brackets Notation
  - Javascript Internal Brackets Notation
  - JavaScript Internal Bracket Notation
  - ECMAScript Double Bracket Notation
  - Double Square Bracket Notation
  - "[[...]] notation"
  - Нотация двойных квадратных скобок
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent: "[[ECMAScript Specification Model]]"
status: seed
related:
  - "[[ECMAScript Internal Slot]]"
  - "[[ECMAScript Internal Method]]"
  - "[[ECMAScript Abstract Operation]]"
  - "[[JavaScript Prototype Internal Slot]]"
  - "[[JavaScript Property Descriptor]]"
tags: []
---

# ECMAScript Internal Bracket Notation

## Краткое определение

`ECMAScript Internal Bracket Notation` — это спецификационная нотация двойных квадратных скобок `[[...]]`, которой стандарт ECMAScript обозначает внутренние методы, внутренние слоты и некоторые поля служебных спецификационных структур.

## Основная идея или механизм

Запись `[[Name]]` не означает обычное свойство объекта JavaScript с ключом `"[[Name]]"`. Это маркер языка спецификации: он показывает, что речь идет о внутренней сущности стандарта, через которую описывается обязательное поведение реализации.

Ключевой пример из объектной модели:

```text
[[Prototype]]
[[Get]]
[[Set]]
[[Value]]
[[Type]]
```

Эти имена могут относиться к разным классам сущностей: `[[Prototype]]` как internal slot объекта, `[[Get]]` как internal method или attribute accessor property descriptor, `[[Value]]` как поле descriptor/record.

## Границы темы

- Входит: чтение записи `[[...]]`, различение спецификационного обозначения и пользовательского синтаксиса, связь с internal slots, internal methods и record fields.
- Не входит: детальное устройство конкретного слота `[[Prototype]]`; оно раскрывается в `[[JavaScript Prototype Internal Slot]]`.
- Не входит: полный алгоритм разрешения свойств; он относится к `[[JavaScript Prototype System]]` и `[[JavaScript Property Model]]`.

## Связи с другими заметками

Родительская тема:

`[[ECMAScript Specification Model]]`

Связанные заметки:

- `[[ECMAScript Internal Slot]]`
- `[[ECMAScript Internal Method]]`
- `[[ECMAScript Abstract Operation]]`
- `[[JavaScript Prototype Internal Slot]]`
- `[[JavaScript Property Descriptor]]`

## Примеры, случаи или следствия

`obj.[[Prototype]]` в тексте спецификации означает внутреннюю прототипную связь объекта, а не синтаксис, который можно выполнить в JavaScript-коде.

`O.[[Get]](P, Receiver)` в алгоритме спецификации означает вызов внутреннего метода объекта, а не обращение к публичному методу `O["[[Get]]"]`.

Descriptor-поля вроде `[[Value]]`, `[[Writable]]`, `[[Get]]` и `[[Set]]` показывают, как стандарт формально описывает состояние свойства, но не являются обычными enumerable-полями пользовательского объекта.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между internal method и descriptor field при одинаковой записи `[[Get]]`
- [ ] Добавить пример с `[[Prototype]]` и `__proto__`
- [ ] Добавить пример с property descriptor
- [ ] Проверить `aliases`
