---
aliases:
  - Composite Types in Go
  - Составные типы Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Type System]]"
status: seed
related:
  - "[[Go Type System]]"
  - "[[Go Basic Types]]"
  - "[[Go Memory Management]]"
tags: []
---

# Go Composite Types

## Краткое определение

Статья о составных типах Go: массивах, срезах, структурах, map, указателях, функциях, каналах и других формах, которые строятся поверх базовой типовой основы.

## Границы темы

- В тему входят canonical composite forms и различия между ними как контейнерами, ссылочными структурами и поведенческими значениями.
- На границе находятся `[[Go Memory Management]]`, потому что часть composite types тесно связана с allocation behavior.

## Связи с другими заметками

Родительская тема:

`[[Go Type System]]`

Связанные заметки:

- `[[Go Basic Types]]`
- `[[Go Defined Types and Underlying Types]]`
- `[[Go Memory Management]]`

## Примеры, случаи или следствия

- Выбор между array, slice и map в Go влияет не только на API, но и на семантику передачи значений.
- Struct types часто становятся базой для methods, interfaces и domain-level modeling.

## Что стоит раскрыть дальше

- [ ] Решить, когда выделять отдельные notes про `slice`, `map`, `struct` и `pointer`
- [ ] Уточнить связь между composite types и zero values
- [ ] Проверить `aliases`
