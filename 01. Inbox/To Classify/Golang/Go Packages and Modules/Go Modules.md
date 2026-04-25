---
aliases:
  - Go Module System
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Packages and Modules]]"
status: draft
related:
  - "[[Go Packages and Modules]]"
  - "[[Go Packages]]"
  - "[[go.mod]]"
  - "[[go mod]]"
tags: []
---

# Go Modules

## Краткое определение

`Go Modules` - это тема о module как единице versioning, dependency management и distribution в Go.

## Основная идея или механизм

Модуль задает верхнюю границу для набора пакетов, фиксирует module path и служит опорой для разрешения зависимостей через файлы module metadata.

## Границы темы

- В тему входят module boundaries, module path и отношение к зависимостям.
- Рядом находится `[[go mod]]`, но она описывает уже operational command interface, а не саму модель модулей.

## Связи с другими заметками

Родительская тема:

`[[Go Packages and Modules]]`

Связанные заметки:

- `[[Go Packages]]`
- `[[go.mod]]`
- `[[go mod]]`

## Примеры, случаи или следствия

Переход от package-only мышления к module-level мышлению особенно важен там, где нужно понимать versioned dependencies и public module boundaries.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между module path и import path
- [ ] Добавить связь с version selection и dependency graph
- [ ] Проверить `related`
