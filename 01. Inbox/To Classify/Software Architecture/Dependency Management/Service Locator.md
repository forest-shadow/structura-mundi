---
aliases: []
note_type: article
area: computer-science
domain: software-architecture
section: dependency-management
parent: "[[Dependency Management]]"
status: seed
related:
  - "[[Dependency Injection]]"
  - "[[Composition Root]]"
tags: []
---

# Service Locator

## Краткое определение

Каноническая статья про подход, при котором объект сам запрашивает зависимости из общего реестра или контейнера, вместо явного получения их извне.

## Основная идея или механизм

`Service Locator` внешне может решать ту же прикладную задачу, что и `Dependency Injection`, но делает зависимости менее явными и ухудшает читаемость контрактов.

## Границы темы

- Входит: паттерн доступа к зависимостям через locator.
- Не входит: общая теория проектных принципов.

## Связи с другими заметками

Родительская тема:

`[[Dependency Management]]`

Связанные заметки:

- `[[Dependency Injection]]`
- `[[Composition Root]]`
