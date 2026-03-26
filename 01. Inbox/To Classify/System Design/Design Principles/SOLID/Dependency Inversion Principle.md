---
aliases:
  - DIP
note_type: article
area: computer-science
domain: system-design
section: design-principles
parent: "[[SOLID]]"
status: seed
related:
  - "[[Dependency Injection]]"
  - "[[Composition Root]]"
  - "[[Service Locator]]"
tags: []
---

# Dependency Inversion Principle

## Краткое определение

Каноническая статья про принцип, согласно которому высокоуровневые модули не должны зависеть от низкоуровневых реализаций напрямую, а обе стороны должны зависеть от абстракций.

## Основная идея или механизм

`DIP` задает направление зависимостей в системе и поэтому особенно тесно связан с `Dependency Injection` и `Composition Root`, которые помогают practically apply этот принцип в приложении.

## Границы темы

- Входит: направление зависимостей и роль абстракций.
- Не входит: конкретный способ wiring-а зависимостей.

## Связи с другими заметками

Родительская тема:

`[[SOLID]]`

Связанные заметки:

- `[[Dependency Injection]]`
- `[[Composition Root]]`
- `[[Service Locator]]`
