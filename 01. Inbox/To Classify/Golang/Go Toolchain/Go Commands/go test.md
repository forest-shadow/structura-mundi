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
  - "[[Go Testing]]"
  - "[[go build]]"
tags: []
---

# go test

## Краткое определение

`go test` - это команда Go для запуска тестов, benchmark-ов и fuzzing-сценариев в рамках стандартной testing model языка.

## Основная идея или механизм

Команда находит тестовые файлы, собирает тестовый binary и выполняет тестовые entry points по правилам пакета `testing`.

## Границы темы

- В тему входит командный интерфейс тестирования и его основные режимы запуска.
- Рядом находится `[[Go Testing]]`, где раскрывается уже более широкая модель тестов, subtests, benchmarks и fuzzing.

## Связи с другими заметками

Родительская тема:

`[[Go Commands]]`

Связанные заметки:

- `[[Go Testing]]`
- `[[go build]]`

## Примеры, случаи или следствия

`go test` важна тем, что делает тестирование встроенной частью стандартного developer workflow, а не внешним add-on.

## Что стоит раскрыть дальше

- [ ] Уточнить роль package patterns и selective runs
- [ ] Уточнить границу между command surface и testing semantics
- [ ] Проверить `related`
