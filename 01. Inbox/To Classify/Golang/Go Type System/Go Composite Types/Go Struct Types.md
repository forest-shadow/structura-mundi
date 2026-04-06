---
aliases:
  - Struct Types in Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Composite Types]]"
status: seed
related:
  - "[[Go Type Literals]]"
  - "[[Go Field Selectors]]"
  - "[[Go Embedded Fields]]"
  - "[[Go Struct Tags]]"
  - "[[Go Reflection Struct Inspection and Tags]]"
tags: []
---

# Go Struct Types

## Определение

`Go Struct Types` - это составные типы Go, которые объединяют набор именованных полей в одну структурированную форму данных.

## Почему это отдельная тема

`struct` - одна из центральных форм моделирования данных в Go. Через неё язык выражает локальную композицию, группировку состояния и основу для многих idiomatic API.

## Что здесь стоит рассматривать

- синтаксис объявления `struct`;
- поля, их имена и типы;
- embedded fields;
- различие между anonymous и named struct types;
- роль struct types в композиции данных.

## Что важно не смешивать

В этой заметке не стоит растворять всё, что связано со структурами вообще. Метаданные полей через теги лучше раскрывать отдельно в [[Go Struct Tags]], а reflection-доступ к полям и тегам - в [[Go Reflection Struct Inspection and Tags]].

## Связи

- Родительская обзорная заметка: [[Go Composite Types]]
- Предпосылка по синтаксису типов: [[Go Type Literals]]
- Смежные темы: [[Go Embedded Fields]], [[Go Field Selectors]], [[Go Struct Tags]]

## Что раскрывать дальше

- различие между literal struct values и named struct types;
- совместимость и identity struct types;
- embedded composition и promoted members;
- отдельную ветку по тегам полей в [[Go Struct Tags]].