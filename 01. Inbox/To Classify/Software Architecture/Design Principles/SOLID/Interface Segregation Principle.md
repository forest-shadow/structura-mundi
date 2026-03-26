---
aliases:
  - ISP
note_type: article
area: computer-science
domain: software-architecture
section: design-principles
parent: "[[SOLID]]"
status: seed
related:
  - "[[Liskov Substitution Principle]]"
  - "[[Dependency Inversion Principle]]"
tags: []
---

# Interface Segregation Principle

## Краткое определение

Каноническая статья про принцип, согласно которому клиентам не следует зависеть от методов, которые они не используют.

## Основная идея или механизм

`ISP` помогает проектировать небольшие и целевые контракты вместо широких интерфейсов, которые тянут за собой лишние зависимости.

## Границы темы

- Входит: форма и размер интерфейсов.
- Не входит: конкретные техники инъекции зависимостей.

## Связи с другими заметками

Родительская тема:

`[[SOLID]]`

Связанные заметки:

- `[[Liskov Substitution Principle]]`
- `[[Dependency Inversion Principle]]`
