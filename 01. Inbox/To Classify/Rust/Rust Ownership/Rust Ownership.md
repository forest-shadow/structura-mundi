---
aliases: []
note_type: overview
area: computer-science
domain: programming-languages
section: rust
parent: "[[Rust]]"
status: seed
related:
  - "[[Rust]]"
  - "[[Rust Borrowing]]"
  - "[[Rust Lifetimes]]"
  - "[[Rust Traits]]"
tags: []
---

# Rust Ownership

## Краткое определение области

`Rust Ownership` — обзорная заметка про центральную модель управления памятью и ресурсами в Rust, из которой естественно вырастают темы borrowing и lifetimes.

## Что входит в эту тему

- `[[Rust Borrowing]]`
- `[[Rust Lifetimes]]`

## Как устроена ветка

- `Rust Ownership` служит локальным `overview` для memory-safety semantics языка.
- Внутри этой ветки `Rust Borrowing` стоит держать как отдельный обзорный узел, потому что именно через него ownership-модель переходит к правилам ссылок и aliasing.
- `Rust Lifetimes` пока лучше держать дочерней `article`, потому что это уже более узкий механизм внутри borrowing-ветки.

## Рекомендуемый маршрут чтения

1. Начать с `Rust Ownership`.
2. Затем перейти к `[[Rust Borrowing]]`.
3. После этого читать `[[Rust Lifetimes]]`.
4. Затем возвращаться к верхнему уровню `Rust` и переходить к `[[Rust Traits]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Rust]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Rust Move Semantics` и `Rust Ownership Transfer`
- [ ] Проверить, когда `Rust Borrowing` начинает требовать отдельных notes про mutable и immutable borrows
- [ ] Проверить `related`
