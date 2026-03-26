---
aliases:
  - OCP
note_type: article
area: computer-science
domain: system-design
section: design-principles
parent: "[[SOLID]]"
status: seed
related:
  - "[[Single Responsibility Principle]]"
  - "[[Dependency Inversion Principle]]"
tags: []
---

# Open-Closed Principle

## Краткое определение

Каноническая статья про принцип, согласно которому модуль должен быть открыт для расширения, но закрыт для модификации уже устойчивого поведения.

## Основная идея или механизм

`OCP` помогает вводить новые варианты поведения через расширение контрактов и компоновку, а не через постоянное переписывание существующего кода.

## Границы темы

- Входит: расширяемость без разрушения существующего поведения.
- Не входит: конкретные DI-механизмы.

## Связи с другими заметками

Родительская тема:

`[[SOLID]]`

Связанные заметки:

- `[[Single Responsibility Principle]]`
- `[[Dependency Inversion Principle]]`
