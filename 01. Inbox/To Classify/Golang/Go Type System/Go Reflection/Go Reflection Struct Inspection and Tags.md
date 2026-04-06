---
aliases:
  - Go Reflection on Structs and Tags
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Go Struct Types]]"
  - "[[Go Struct Tags]]"
  - "[[Go Runtime Type Information]]"
tags: []
---

# Go Reflection Struct Inspection and Tags

## Определение

`Go Reflection Struct Inspection and Tags` - это рассмотрение того, как reflection в Go позволяет исследовать структуру `struct`-типов и читать теги их полей во время выполнения.

## Почему это отдельная тема

Reflection делает возможным runtime-доступ к форме `struct`, списку полей, embedded members и строковым тегам. Это особенно важно для сериализации, ORM-подходов, validation frameworks и generic tooling.

## Что здесь стоит рассматривать

- получение `reflect.Type` и `reflect.Value` для структур;
- обход полей структуры;
- чтение `StructField.Tag` и работу с `.Get(...)`;
- различие между exported и unexported полями в reflection-context;
- типичные ограничения и подводные камни.

## Что важно не смешивать

Языковая природа тегов как части объявления `struct` лучше раскрывается отдельно в [[Go Struct Tags]]. Эта заметка должна концентрироваться на runtime-inspection перспективе: как теги и поля извлекаются, а не на том, почему теги как механизм существуют в языке.

## Связи

- Родительская обзорная заметка: [[Go Reflection]]
- Ближайшая языковая тема: [[Go Struct Types]]
- Специальная заметка о самих тегах: [[Go Struct Tags]]
- Смежная тема: [[Go Runtime Type Information]]

## Что раскрывать дальше

- различие между `Type` и `Value` при работе со структурами;
- чтение тегов и field metadata;
- адресуемость и settable semantics;
- ошибки проектирования, где reflection используется вместо более простых механизмов.