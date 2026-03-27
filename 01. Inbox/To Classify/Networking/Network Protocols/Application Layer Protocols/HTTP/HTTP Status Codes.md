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
  - "[[HTTP Methods]]"
tags: []
---

# HTTP Status Codes

## Краткое определение

`HTTP Status Codes` — это статья о кодах ответа, через которые сервер сообщает общий результат обработки HTTP-запроса.

## Границы темы

- Входит: статусные классы и их роль в response semantics.
- Не входит: полный справочник по каждому коду как по отдельной note.

## Связи с другими заметками

Родительская тема:

`[[HTTP]]`

Связанные заметки:

- `[[HTTP Messages]]`
- `[[HTTP Methods]]`

## Примеры, случаи или следствия

- Классы `2xx`, `3xx`, `4xx` и `5xx` дают первичную карту результатов без разбора каждого частного кода.
- Статус-коды влияют на обработку ошибок, redirects, retries и caching behavior.

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужен отдельный раздел про status code classes
- [ ] Проверить `related`
