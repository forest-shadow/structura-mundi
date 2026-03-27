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
  - "[[HTTP Status Codes]]"
tags: []
---

# HTTP Methods

## Краткое определение

`HTTP Methods` — это статья о методах запроса как способах обозначить намерение клиента по отношению к целевому ресурсу.

## Границы темы

- Входит: methods как часть HTTP request semantics.
- Не входит: полный практический разбор каждого endpoint design style.

## Связи с другими заметками

Родительская тема:

`[[HTTP]]`

Связанные заметки:

- `[[HTTP Messages]]`
- `[[HTTP Status Codes]]`

## Примеры, случаи или следствия

- Методы помогают различать чтение, создание, обновление и удаление на уровне протокольного намерения.
- Свойства вроде safety и idempotency влияют на caching, retries и клиентское поведение.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный раздел про safe и idempotent methods
- [ ] Проверить `related`
