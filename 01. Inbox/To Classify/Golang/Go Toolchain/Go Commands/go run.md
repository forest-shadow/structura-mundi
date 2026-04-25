---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Commands]]"
status: draft
related:
  - "[[Go Commands]]"
  - "[[Go Toolchain]]"
  - "[[go build]]"
tags: []
---

# go run

## Краткое определение

`go run` - это команда Go для быстрого запуска программы через compile-and-execute workflow без отдельного ручного шага запуска собранного бинарника.

## Основная идея или механизм

Команда собирает указанный пакет или набор файлов во временный executable и сразу передает управление выполняемой программе.

## Границы темы

- В тему входит быстрый локальный запуск и exploratory workflow.
- Рядом находится `[[go build]]`, но она отделяет сборку от исполнения.

## Связи с другими заметками

Родительская тема:

`[[Go Commands]]`

Связанные заметки:

- `[[Go Toolchain]]`
- `[[go build]]`

## Примеры, случаи или следствия

`go run` особенно полезен для небольших CLI, playground-like сценариев и быстрой проверки изменений.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между запуском package path и списком файлов
- [ ] Уточнить ограничения для production workflow
- [ ] Проверить `related`
