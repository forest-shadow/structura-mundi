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
  - "[[Go Packages and Modules]]"
  - "[[Go Toolchain]]"
tags: []
---

# go mod

## Краткое определение

`go mod` - это семейство команд Go для управления модулем, зависимостями и связанными metadata файлами проекта.

## Основная идея или механизм

Команда работает с module graph и файлами вроде `go.mod` и `go.sum`, позволяя объявлять, разрешать и обслуживать зависимости в рамках стандартной module system Go.

## Границы темы

- В тему входят основные операции command surface для module management.
- Рядом находится `[[Go Packages and Modules]]`, где описывается сама модель пакетов, модулей и import organization.

## Связи с другими заметками

Родительская тема:

`[[Go Commands]]`

Связанные заметки:

- `[[Go Packages and Modules]]`
- `[[Go Toolchain]]`

## Примеры, случаи или следствия

`go mod` делает dependency management встроенной частью стандартного toolchain и снижает зависимость от внешних package managers.

## Что стоит раскрыть дальше

- [ ] Уточнить, какие подкоманды заслуживают отдельных статей
- [ ] Добавить связь с module graph и reproducibility
- [ ] Проверить `related`
