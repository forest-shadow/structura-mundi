---
aliases:
  - Type, Value, and Kind in Go Reflection
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Go Defined Types and Underlying Types]]"
  - "[[Go Interfaces]]"
  - "[[Addressability and Settable Values in Go Reflection]]"
tags: []
---

# reflect.Type, reflect.Value and reflect.Kind

## Краткое определение

Статья о трех центральных runtime-сущностях reflection в Go: `reflect.Type`, `reflect.Value` и `reflect.Kind`, через которые язык предоставляет доступ к типовой информации и данным во время выполнения.

## Основная идея или механизм

Reflection в Go не работает с типами и значениями напрямую из синтаксиса программы. Вместо этого она оперирует runtime-объектами, которые описывают тип, текущее значение и его категорию. Именно здесь проходит граница между named type, конкретным value и более грубой классификацией через kind.

## Границы темы

- В тему входят `TypeOf`, `ValueOf`, `Kind`, `Interface`, `Elem`, `Indirect`, `Zero`, `New` и различие между type identity и kind classification.
- На границе находятся mutation-операции и ограничения settable values, которые лучше раскрывать в отдельной заметке.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[Go Defined Types and Underlying Types]]`
- `[[Go Interfaces]]`
- `[[Addressability and Settable Values in Go Reflection]]`

## Примеры, случаи или следствия

- Два типа могут иметь один и тот же `Kind`, но оставаться разными named types с разной identity.
- Reflection видит runtime-представление значений, но это не означает полной отмены типовой модели Go.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между `Type`, `Kind` и underlying type
- [ ] Добавить роль `Interface()`, `Elem()` и `Indirect()`
- [ ] Проверить `related`
