---
aliases:
  - Go Package Import Paths
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Packages and Modules]]"
status: draft
related:
  - "[[Go Packages and Modules]]"
  - "[[Go Packages]]"
  - "[[Go Modules]]"
tags: []
---

# Go Import Paths

## Краткое определение

`Go Import Paths` - это тема о том, как Go идентифицирует и адресует импортируемые пакеты через строковые пути.

## Основная идея или механизм

Import path связывает package usage в коде с module layout и местом пакета в dependency graph.

## Границы темы

- В тему входят import path identity, связь с package name и отношение к module path.
- Рядом находится `[[Go Packages]]`, но она описывает package как единицу кода, а не как адресуемую ссылку.

## Связи с другими заметками

Родительская тема:

`[[Go Packages and Modules]]`

Связанные заметки:

- `[[Go Packages]]`
- `[[Go Modules]]`

## Примеры, случаи или следствия

Непонимание import paths часто приводит к путанице между именем пакета, путем модуля и фактической структурой каталогов.

## Что стоит раскрыть дальше

- [ ] Уточнить различие import path, module path и package name
- [ ] Добавить типовые случаи для internal и nested packages
- [ ] Проверить `related`
