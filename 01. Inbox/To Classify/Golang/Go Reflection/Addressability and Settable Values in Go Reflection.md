---
aliases:
  - Addressability in Go Reflection
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[reflect.Type, reflect.Value and reflect.Kind]]"
  - "[[Dynamic Operations in Go Reflection]]"
  - "[[Go Defined Types and Underlying Types]]"
tags: []
---

# Addressability and Settable Values in Go Reflection

## Краткое определение

Статья о том, как в Go Reflection различаются addressable и settable values и почему именно эти ограничения определяют, можно ли безопасно менять значение через `reflect.Value`.

## Основная идея или механизм

Наличие `reflect.Value` еще не означает, что значение можно изменить. Reflection в Go различает просто наблюдаемое значение, адресуемое значение и значение, которое разрешено менять через API. Это различие определяет поведение `CanAddr`, `CanSet`, `Elem()` и объясняет типичные panic-сценарии.

## Границы темы

- В тему входят addressability, settable values, `CanAddr`, `CanSet`, указатели, `Elem()` и ограничения на изменение неэкспортируемых полей.
- На границе находятся сами mutation-операции `Set*`, которые лучше раскрывать в `[[Dynamic Operations in Go Reflection]]`.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[reflect.Type, reflect.Value and reflect.Kind]]`
- `[[Dynamic Operations in Go Reflection]]`
- `[[Struct Inspection and Tags in Go Reflection]]`

## Примеры, случаи или следствия

- `ValueOf(x)` и `ValueOf(&x).Elem()` ведут себя по-разному, потому что только второй путь обычно дает доступ к settable value.
- Большинство неожиданностей reflection связаны не с типами как таковыми, а с нарушением правил addressability и exported access.

## Что стоит раскрыть дальше

- [ ] Добавить типичные причины panic при `Set*`
- [ ] Уточнить работу с указателями и неэкспортируемыми полями
- [ ] Проверить `related`
