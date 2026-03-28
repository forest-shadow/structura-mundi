---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: rust
parent: "[[Rust]]"
status: seed
related:
  - "[[Rust Traits]]"
  - "[[Unsafe Rust]]"
  - "[[Rust Cargo and Toolchain]]"
tags: []
---

# Rust Enums and Pattern Matching

## Краткое определение

`Rust Enums and Pattern Matching` — это узел про algebraic data types и механизм разбора вариантов значения, через которые Rust выражает безопасные разветвления логики и моделирует сложные состояния.

## Основная идея или механизм

Enums в Rust задают тип, значение которого может принадлежать одному из нескольких вариантов, а pattern matching позволяет явно и исчерпывающе разобрать эти варианты. Вместе они образуют одну из ключевых выразительных частей языка: позволяют кодировать ошибки, состояния, сообщения и переходы без неявных null-like договоренностей.

## Границы темы

- В эту тему входит: enum как sum type, variants, `match`, destructuring и exhaustiveness checking.
- Рядом, но не тождественно ей: structs, traits, generics, `Option`, `Result` и макросы.

## Связи с другими заметками

Родительская тема:

`[[Rust]]`

Связанные заметки:

- `[[Rust Traits]]`
- `[[Unsafe Rust]]`
- `[[Rust Cargo and Toolchain]]`

## Примеры, случаи или следствия

- `Option<T>` и `Result<T, E>` являются каноническими примерами enum-centric дизайна в Rust.
- `match` заставляет явно обработать все существенные варианты значения.
- Pattern matching делает безопаснее переход от data model к control flow.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужно делить тему на `Rust Enums` и `Rust Pattern Matching`
- [ ] Проверить, когда нужны отдельные notes про `Option` и `Result`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
