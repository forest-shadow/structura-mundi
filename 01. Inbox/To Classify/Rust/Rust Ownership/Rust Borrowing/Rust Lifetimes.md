---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: rust
parent: "[[Rust Borrowing]]"
status: seed
related:
  - "[[Rust Borrowing]]"
  - "[[Rust Ownership]]"
  - "[[Rust Traits]]"
tags: []
---

# Rust Lifetimes

## Краткое определение

`Rust Lifetimes` — это механизм, через который Rust выражает, как долго ссылки остаются корректными и какие отношения времени жизни допустимы между значениями и заимствованиями.

## Основная идея или механизм

Lifetimes не описывают «время жизни объекта» в runtime-смысле, а формализуют правила корректности ссылок на уровне компилятора. Через них Rust проверяет, что ссылка не переживает данные, на которые она указывает, и что borrowing-семантика не нарушается в функциях, структурах и API.

## Границы темы

- В эту тему входит: lifetimes как часть borrowing-модели, lifetime annotations, их роль в сигнатурах и типах.
- Рядом, но не тождественно ей: ownership в целом, borrow checker diagnostics, higher-ranked trait bounds и unsafe lifetime-manipulation.

## Связи с другими заметками

Родительская тема:

`[[Rust Borrowing]]`

Связанные заметки:

- `[[Rust Ownership]]`
- `[[Rust Traits]]`

## Примеры, случаи или следствия

- Функция, возвращающая ссылку, часто должна явно показать, с каким входным заимствованием связан результат.
- Структура, хранящая ссылки, обычно делает lifetime частью своего типа.
- Ошибки компилятора про «borrowed value does not live long enough» обычно раскрывают именно lifetime-ограничения.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между lifetime elision и явными annotations
- [ ] Решить, когда нужна отдельная note про higher-ranked lifetimes
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
