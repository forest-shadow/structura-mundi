---
aliases: []
note_type: article
area: computer-science
domain: networking
section: network-protocols
parent: "[[HTTP]]"
status: seed
related:
  - "[[HTTP]]"
  - "[[HTTP Messages]]"
  - "[[HTTP Versions]]"
tags: []
---

# HTTP Header Fields

## Краткое определение

`HTTP Header Fields` — это статья о заголовках HTTP как механизме передачи метаданных о сообщении, ресурсе, содержимом и поведении клиента или сервера.

## Границы темы

- Входит: headers как общий слой метаданных в HTTP.
- Не входит: полный каталог каждого стандартного и нестандартного header field.

## Связи с другими заметками

Родительская тема:

`[[HTTP]]`

Связанные заметки:

- `[[HTTP Messages]]`
- `[[HTTP Versions]]`

## Примеры, случаи или следствия

- Через headers передаются сведения о типе содержимого, кэшировании, согласовании представлений и аутентификации.
- Именно headers часто несут значительную часть practical HTTP semantics помимо метода и status code.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Content-Type`, `Cache-Control` и `Authorization`
- [ ] Проверить `related`
