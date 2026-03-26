---
aliases:
  - IoC
note_type: article
area: computer-science
domain: system-design
section: dependency-management
parent: "[[Dependency Management]]"
status: seed
related:
  - "[[Dependency Injection]]"
  - "[[Service Locator]]"
tags: []
---

# Inversion of Control

## Краткое определение

Каноническая статья про общий архитектурный принцип, при котором создание и предоставление зависимостей выносится из бизнес-объектов во внешний управляющий слой.

## Основная идея или механизм

`IoC` задает общую рамку, внутри которой `Dependency Injection` и другие техники решают вопрос, кто именно создает и связывает зависимости.

## Границы темы

- Входит: общая идея инверсии контроля.
- Не входит: конкретная реализация composition root.

## Связи с другими заметками

Родительская тема:

`[[Dependency Management]]`

Связанные заметки:

- `[[Dependency Injection]]`
- `[[Service Locator]]`
