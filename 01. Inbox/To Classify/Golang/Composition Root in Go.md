---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Composition Root]]"
  - "[[Dependency Injection]]"
  - "[[Go]]"
tags: []
---

# Composition Root in Go

## Краткое определение

Каноническая статья про идиоматичную реализацию `Composition Root` в Go, где сборка зависимостей обычно сосредоточена в `main` package или другом внешнем слое запуска приложения.

## Основная идея или механизм

В Go composition root обычно строится через manual DI, явные конструкторы и простое wiring на границе программы, а не через тяжелые контейнеры.

## Границы темы

- Входит: `main.go`, constructor wiring и идиоматичный manual DI.
- Не входит: общая теория `Composition Root` вне Go.

## Связи с другими заметками

Родительская тема:

`[[Go]]`

Связанные заметки:

- `[[Composition Root]]`
- `[[Dependency Injection]]`
