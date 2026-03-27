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
  - "[[HTTP Methods]]"
  - "[[HTTP Header Fields]]"
  - "[[HTTP Status Codes]]"
tags: []
---

# HTTP Messages

## Краткое определение

`HTTP Messages` — это статья о структуре HTTP requests и responses как базовых единиц обмена в протоколе.

## Границы темы

- Входит: request-response message model, стартовая линия и общая роль headers и body.
- Не входит: полный каталог всех методов, заголовков и кодов статуса.

## Связи с другими заметками

Родительская тема:

`[[HTTP]]`

Связанные заметки:

- `[[HTTP Methods]]`
- `[[HTTP Header Fields]]`
- `[[HTTP Status Codes]]`

## Примеры, случаи или следствия

- Без модели request и response остальные части HTTP остаются набором несвязанных элементов.
- Message structure помогает понять, где именно живут method, status code, headers и body.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный раздел про request target и message body
- [ ] Проверить `related`
