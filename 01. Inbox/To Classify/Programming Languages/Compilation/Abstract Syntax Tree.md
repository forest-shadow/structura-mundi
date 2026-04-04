---
aliases:
  - AST
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Parsing]]"
  - "[[Semantic Analysis]]"
  - "[[Program Translation Pipeline]]"
tags: []
---

# Abstract Syntax Tree

## Краткое определение

`Abstract Syntax Tree` — это древовидное структурное представление программы, в котором сохраняется синтаксическая форма, существенная для дальнейшего анализа и трансляции, но убираются многие поверхностные детали исходного текста.

## Основная идея или механизм

AST нужен как более удобная форма программы после parsing: по нему выполняют semantic analysis, преобразования, оптимизации и дальнейшую генерацию кода.

## Границы темы

- Входит: узлы дерева, структурное представление выражений и операторов, роль AST между parsing и semantic analysis.
- Не входит: весь parsing целиком, а также конкретные IR lowerings и machine-specific code generation.

## Связи с другими заметками

Родительская тема:

`[[Compilation]]`

Связанные заметки:

- `[[Parsing]]`
- `[[Semantic Analysis]]`
- `[[Program Translation Pipeline]]`

## Примеры, случаи или следствия

Одна и та же программа как текст удобна для чтения человеком, но неудобна для анализа. AST превращает её в форму, где выражение, вызов функции или условная конструкция уже представлены как явно различимые узлы.

## Что стоит раскрыть дальше

- [ ] Уточнить отличие AST от parse tree
- [ ] Добавить примеры дерева для простых выражений
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
