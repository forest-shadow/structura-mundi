---
aliases:
  - LSP
note_type: article
area: computer-science
domain: system-design
section: design-principles
parent: "[[SOLID]]"
status: seed
related:
  - "[[Interface Segregation Principle]]"
tags: []
---

# Liskov Substitution Principle

## Краткое определение

Каноническая статья про принцип, согласно которому подтип должен быть взаимозаменяем с базовым контрактом без нарушения ожидаемого поведения системы.

## Основная идея или механизм

`LSP` защищает систему от таких абстракций, при которых формальная совместимость типов есть, а поведенческая совместимость нарушена.

## Границы темы

- Входит: контрактная и поведенческая подстановка.
- Не входит: общая теория типов.

## Связи с другими заметками

Родительская тема:

`[[SOLID]]`

Связанные заметки:

- `[[Interface Segregation Principle]]`
