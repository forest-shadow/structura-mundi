---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: rust
parent: "[[Rust]]"
status: seed
related:
  - "[[Rust Enums and Pattern Matching]]"
  - "[[Rust Cargo and Toolchain]]"
  - "[[Rust Traits]]"
tags: []
---

# Unsafe Rust

## Краткое определение

`Unsafe Rust` — это часть языка, в которой разработчик вручную берет на себя ответственность за соблюдение инвариантов, которые обычно гарантируются безопасным подмножеством Rust.

## Основная идея или механизм

Unsafe Rust не отменяет общую модель языка, а открывает ограниченные точки выхода из нее: raw pointers, вызовы unsafe-функций, доступ к mutable static, реализацию unsafe-traits и определенные операции с union. Этот слой нужен там, где безопасный Rust сам по себе недостаточен для низкоуровневого контроля, FFI или построения собственных безопасных абстракций поверх опасных примитивов.

## Границы темы

- В эту тему входит: что именно делает код unsafe, зачем это нужно и какие инварианты разработчик обязан поддерживать сам.
- Рядом, но не тождественно ей: safe abstractions, ownership и borrowing в общем виде, concurrency guarantees и build tooling.

## Связи с другими заметками

Родительская тема:

`[[Rust]]`

Связанные заметки:

- `[[Rust Enums and Pattern Matching]]`
- `[[Rust Cargo and Toolchain]]`
- `[[Rust Traits]]`

## Примеры, случаи или следствия

- FFI-обертки часто содержат локальные unsafe-блоки внутри безопасного внешнего API.
- Низкоуровневые контейнеры и allocators могут требовать unsafe-кода для внутренней реализации.
- Качество unsafe-кода определяется не только тем, что он компилируется, но и тем, насколько четко сформулированы его invariants.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужна отдельная note про raw pointers
- [ ] Решить, когда нужна отдельная note про unsafe abstractions and invariants
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
