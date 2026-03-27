---
aliases:
  - Go Non-Canonical Type Taxonomies
  - Informal Type Taxonomies in Go
  - Неканоничные таксономии типов Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Assignability and Conversions]]"
  - "[[Go Interfaces]]"
  - "[[Go Type Parameters and Constraints]]"
  - "[[Go Composite Types]]"
tags: []
---

# Go Informal Type Taxonomies

## Краткое определение

Статья о неканоничных, но полезных учебных классификациях типов в Go: по поведению при копировании, nilability, сравнимости и роли в generics. Это не formal taxonomy языка, а вторичный объяснительный слой, который помогает быстрее видеть практические инварианты поверх канонической модели.

## Основная идея или механизм

Спецификация Go задает типовую систему через canonical categories вроде basic types, composite types, defined types, interfaces, assignability и type parameters. Поверх этой модели удобно строить дополнительные учебные таксономии, которые пересекают формальные категории и отвечают на прикладные вопросы: что nilable, что comparable, что при копировании может продолжать делить underlying state и что можно использовать только как constraint.

## Границы темы

- В тему входят только вторичные, учебные классификации типов и объяснение того, почему они полезны, но неканоничны.
- На границе находятся formal categories языка, которые должны оставаться первичной моделью для спецификации, интервью и точных технических формулировок.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Assignability and Conversions]]`
- `[[Go Interfaces]]`
- `[[Go Type Parameters and Constraints]]`
- `[[Go Composite Types]]`

## Таксономия по поведению при копировании

Учебная идея:

какие типы обычно ведут себя как self-contained copied values, а какие при копировании могут продолжать указывать на общее underlying state или runtime state.

Полезная схема:

- self-contained values: `bool`, numeric types, array, struct
- values with indirect or shared backing/runtime state: slice, map, channel, function, interface
- explicit indirection: pointer
- special immutable descriptor-like value: string

Почему это полезно:

- помогает быстро объяснить, почему присваивание slice не похоже на независимое глубокое копирование;
- помогает увидеть, почему копирование массива ближе к копированию содержимого;
- удобно для первичного объяснения aliasing и shared backing behavior.

Почему это неканонично:

- в спецификации нет официальной верхнеуровневой категории `reference types`;
- slice, map, channel, function, interface и pointer являются разными формальными видами типов;
- эта схема скрывает важные различия их representation и semantics.

## Таксономия по nilability

Учебная идея:

какие типы допускают `nil`, а какие нет.

Полезная схема:

- nilable: pointer, function, slice, map, channel, interface
- non-nilable: bool, numerics, string, array, struct

Почему это полезно:

- помогает запоминать zero values;
- упрощает API-design рассуждения о допустимости `nil`;
- полезно для чтения сигнатур, проверок и guard conditions.

Почему это неканонично:

- nilability является свойством группы типов, а не отдельной top-level family в Go;
- она не заменяет каноническую декомпозицию типовой системы.

## Таксономия по сравнимости

Учебная идея:

разделить типы по тому, работают ли над ними `==` и `!=`.

Полезная схема:

- обычно сравнимые: bool, numerics, pointers, channels, strings, arrays of comparable elements, structs of comparable fields
- несравнимые напрямую: slices, maps, functions
- особый случай: interfaces, сравнение которых зависит от динамического значения и может паниковать
- constraint-level special case: `comparable`

Почему это полезно:

- помогает понимать правила для `map` keys;
- полезно для generics constraints;
- дает быстрый способ проверить, допустимы ли сравнения на уровне операторов.

Почему это неканонично:

- comparability является свойством типа, а не самостоятельной официальной семьей;
- она пересекает canonical categories, а не заменяет их.

## Таксономия по роли в generics

Учебная идея:

разделить типы на обычные value-capable forms и interface forms, которые существуют прежде всего как часть constraint machinery.

Полезная схема:

- ordinary value-capable types: обычные non-interface concrete types и basic interfaces
- constraint-oriented interface forms: `comparable`, interfaces с `~T`, interfaces с unions, non-basic interfaces

Почему это полезно:

- помогает понять, почему `interface{ ~int | ~string }` не является обычным типом значения;
- связывает interfaces с type sets и современным generic-контекстом Go;
- исправляет слишком старую, до-generics картину типовой системы.

Почему это неканонично:

- это вторичная классификация по области применения, а не formal decomposition языка;
- она описывает mode of use, а не базовую taxonomy всех типов Go.

## Зачем такие схемы вообще нужны

- Они помогают быстро схватывать поведенческие инварианты, которые пересекают разные формальные категории.
- Они полезны для запоминания nil-checks, comparability, map-key restrictions, copy semantics и constraint-only forms.
- Они хорошо работают как учебные конспекты и объяснительные shortcuts, если строятся поверх канонической модели, а не вместо нее.

## Почему на интервью лучше держаться канонической модели

- Интервьюер может проверять именно точность языка, а не бытовые эвристики, поэтому формулировки вроде `reference types in Go` создают ненужный риск.
- Неканоничные схемы часто скрывают различия между slice, map, interface, function и pointer, хотя формальная модель языка специально их не сливает.
- В современном Go generics встроены в саму типовую систему, поэтому старая неформальная картина без type sets, `comparable` и non-basic interfaces быстро теряет точность.

## Примеры, случаи или следствия

- Полезно сначала описать тип как canonical category, а уже потом добавлять учебную эвристику вроде `nilable` или `comparison-friendly`.
- Формулировка `slice is a reference type` удобна для запоминания, но технически слабее, чем объяснение через value semantics и shared underlying array.
- Интерфейсы особенно легко неправильно классифицировать, если смешивать ordinary interface values и constraint-only interface forms.

## Что стоит раскрыть дальше

- [ ] Уточнить связь этой заметки с `Go Zero Value and Nil`, если такая note появится
- [ ] Проверить, когда отдельно нужна заметка про `comparable` и non-basic interfaces
- [ ] Проверить `related`
