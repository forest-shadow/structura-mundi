---
aliases:
  - defer
note_type: article
area: computer-science
domain: web-platform
section: script-loading-and-execution
parent: "[[Script Loading and Execution Attributes]]"
status: seed
related:
  - "[[HTML Script Async Attribute]]"
tags:
  - web
  - performance
---

# Defer Script

## Краткое определение

Каноническая статья про атрибут `defer` у `<script>`, который позволяет браузеру загружать внешний скрипт параллельно с парсингом HTML, но откладывает исполнение до завершения парсинга документа.

## Основная идея или механизм

`defer` помогает не блокировать парсинг во время загрузки и при этом сохранять более предсказуемую модель исполнения, чем `async`. Поэтому он чаще подходит для основного кода страницы.

## Границы темы

- Входит: поведение `defer` при загрузке и исполнении external scripts.
- Не входит: общий разбор resource hints.

## Связи с другими заметками

Родительская тема:

`[[Script Loading and Execution Attributes]]`

Связанные заметки:

- `[[Async Script]]`

## Примеры, случаи или следствия

Обычно полезен для основного прикладного скрипта, которому нужен уже распарсенный DOM и предсказуемый порядок относительно других отложенных скриптов.

## Что стоит раскрыть дальше

- [ ] Добавить сравнение с `async`
- [ ] Уточнить связь с `DOMContentLoaded`
- [ ] Проверить `aliases`
