---
aliases:
  - Go Package
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Packages and Modules]]"
status: draft
related:
  - "[[Go Packages and Modules]]"
  - "[[Go Import Paths]]"
  - "[[Go Modules]]"
tags: []
---

# Go Packages

## Краткое определение

`Go Packages` - это тема о package как базовой единице организации, namespace и compilation boundary в Go.

## Основная идея или механизм

Package объединяет набор исходных файлов под одним именем и определяет, какие идентификаторы доступны внутри пакета и какие экспортируются наружу.

## Границы темы

- В тему входят package clause, package-level organization и экспортируемые идентификаторы.
- Рядом находится `[[Go Modules]]`, но module работает уже на уровне версионирования и зависимостей.

## Связи с другими заметками

Родительская тема:

`[[Go Packages and Modules]]`

Связанные заметки:

- `[[Go Import Paths]]`
- `[[Go Modules]]`

## Примеры, случаи или следствия

Границы package напрямую влияют на API surface, читаемость imports и удобство переиспользования кода.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между package name и import path
- [ ] Добавить связь с exports и visibility
- [ ] Проверить `related`
