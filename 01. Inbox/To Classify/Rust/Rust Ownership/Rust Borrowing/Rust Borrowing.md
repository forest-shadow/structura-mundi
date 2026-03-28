---
aliases: []
note_type: overview
area: computer-science
domain: programming-languages
section: rust
parent: "[[Rust Ownership]]"
status: seed
related:
  - "[[Rust Ownership]]"
  - "[[Rust Lifetimes]]"
  - "[[Rust Traits]]"
tags: []
---

# Rust Borrowing

## Краткое определение области

`Rust Borrowing` — обзорный узел про правила временного доступа к значениям без передачи владения, через которые Rust обеспечивает безопасность ссылок и контролирует aliasing.

## Что входит в эту тему

- `[[Rust Lifetimes]]`

## Как устроена ветка

- `Rust Borrowing` связывает общую ownership-модель с практическими правилами работы со ссылками.
- `Rust Lifetimes` здесь выступает как дочерняя explanatory-note про то, как язык формализует длительность допустимых заимствований.
- Пока ветку не стоит дробить глубже, если рядом еще нет устойчивого корпуса заметок про borrow checker diagnostics и reborrowing.

## Рекомендуемый маршрут чтения

1. Начать с `Rust Borrowing` после `[[Rust Ownership]]`.
2. Затем перейти к `[[Rust Lifetimes]]`.
3. После этого возвращаться к более широким языковым механизмам вроде `[[Rust Traits]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Rust Ownership]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужны отдельные notes про mutable borrowing и shared borrowing
- [ ] Проверить, когда нужны notes про borrow checker errors и reborrowing
- [ ] Проверить `related`
