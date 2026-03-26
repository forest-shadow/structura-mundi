---
aliases: []
note_type: article
area: computer-science
domain: software-architecture
section: architecture-patterns
parent: "[[Software Architecture]]"
status: seed
related:
  - "[[Dependency Inversion Principle]]"
  - "[[Composition Root]]"
tags: []
---

# Clean Architecture

## Краткое определение

Каноническая статья про архитектурную рамку, в которой зависимости направляются внутрь к более стабильным слоям, а бизнес-правила отделяются от деталей инфраструктуры.

## Основная идея или механизм

`Clean Architecture` полезно держать рядом с `SOLID` и `Dependency Management`, потому что она часто опирается на `Dependency Inversion Principle` и на явную сборку приложения через composition root.

## Границы темы

- Входит: слои, направление зависимостей и отделение бизнес-логики от инфраструктуры.
- Не входит: полный набор language-specific приемов.

## Связи с другими заметками

Родительская тема:

`[[Software Architecture]]`

Связанные заметки:

- `[[Dependency Inversion Principle]]`
- `[[Composition Root]]`
