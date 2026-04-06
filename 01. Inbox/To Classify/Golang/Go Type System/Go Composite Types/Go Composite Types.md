---
aliases:
  - Composite Types in Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: draft
related:
  - "[[Go Type Literals]]"
  - "[[Go Type Definitions]]"
  - "[[Go Type Identity]]"
  - "[[Go Type Constraints]]"
tags: []
---

# Go Composite Types

## Определение

`Go Composite Types` - это составные типы языка Go, которые строятся из других типов или значений формы типа и задают более сложную организацию данных, чем одиночные базовые значения.

## Почему это отдельная тема

Именно на уровне composite types становится видно, как Go описывает контейнеры, последовательности, структуры и связи между значениями. Здесь язык переходит от отдельных primitive-like типов к способам группировать данные и задавать форму объектов программы.

## Что входит в эту ветку

- [[Go Array Types]]
- [[Go Slice Types]]
- [[Go Map Types]]
- [[Go Struct Types]]
- [[Go Struct Tags]]
- [[Go Pointer Types]]
- [[Go Function Types]]
- [[Go Interface Types]]
- [[Go Channel Types]]

## Как устроена ветка

Эту ветку удобно читать как переход от синтаксической формы type literals к конкретным составным формам данных.

`[[Go Struct Types]]` объясняет, как в Go описывается структура данных через именованные поля. `[[Go Struct Tags]]` фиксирует отдельный языковой механизм метаданных на уровне полей структуры и связывает форму `struct` с практиками сериализации, маппинга и reflection-based inspection.

## Что важно не смешивать

`Go Composite Types` не равны только контейнерам. В эту ветку входят и такие формы, как `struct`, `interface`, `func` и `chan`, то есть любые типовые конструкции, где значима внутренняя композиция.

Также не стоит смешивать описание composite types с их runtime-поведением. Поведение значений, identity, assignability, method sets и reflection должно раскрываться в соседних ветках, а не растворяться внутри обзора по составным типам.

## Связи

- Родительская обзорная заметка: [[Go Type System]]
- Предпосылка по синтаксису типов: [[Go Type Literals]]
- Смежные темы: [[Go Type Identity]], [[Go Type Definitions]], [[Go Type Constraints]]

## Что раскрывать дальше

- различие между value shape и reference-like поведением у разных composite types;
- как composite types участвуют в assignability и comparability;
- чем структурные формы отличаются по semantics и runtime-cost;
- какие ветки требуют отдельных deeper-dive заметок.