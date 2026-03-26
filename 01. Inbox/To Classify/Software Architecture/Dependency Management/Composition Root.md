---
aliases: []
note_type: article
area: computer-science
domain: software-architecture
section: dependency-management
parent: "[[Dependency Injection]]"
status: seed
related:
  - "[[Dependency Inversion Principle]]"
  - "[[Inversion of Control]]"
  - "[[Service Locator]]"
  - "[[Composition Root in Go]]"
tags: []
---

# Composition Root

## Краткое определение

Каноническая статья про архитектурную практику, согласно которой сборка приложения и связывание concrete dependencies должны быть сосредоточены в одной явной точке на границе системы.

## Основная идея или механизм

`Composition Root` не входит в `SOLID` сам по себе, но тесно связан с `Dependency Inversion Principle`, потому что помогает practically apply DI и удерживать направление зависимостей под контролем.

## Границы темы

- Входит: место сборки приложения, wiring зависимостей и построение object graph.
- Не входит: language-specific idioms конкретного языка.

## Связи с другими заметками

Родительская тема:

`[[Dependency Injection]]`

Связанные заметки:

- `[[Dependency Inversion Principle]]`
- `[[Inversion of Control]]`
- `[[Service Locator]]`
- `[[Composition Root in Go]]`
