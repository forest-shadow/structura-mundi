---
aliases: []
note_type: article
area: computer-science
domain: web-platform
section: cors
parent: "[[CORS]]"
status: seed
related:
  - "[[Preflight Request]]"
  - "[[CORS Request Headers]]"
  - "[[Credentialed CORS Requests]]"
tags:
  - web
  - security
---

# CORS Response Headers

## Краткое определение

Каноническая статья про response-headers, через которые сервер сообщает браузеру, разрешён ли cross-origin доступ и на каких условиях.

## Основная идея или механизм

Эта заметка должна объяснять, как сервер через access-control response headers формирует разрешение или запрет для браузера.

## Границы темы

- Входит: роль response-headers в CORS-механизме.
- Не входит: общая теория browser security вне CORS.

## Связи с другими заметками

Родительская тема:

`[[CORS]]`

Связанные заметки:

- `[[Preflight Request]]`
- `[[CORS Request Headers]]`
- `[[Credentialed CORS Requests]]`

## Примеры, случаи или следствия

Добавить примеры `Access-Control-Allow-Origin`, `Access-Control-Allow-Methods`, `Access-Control-Allow-Headers`, `Access-Control-Allow-Credentials`.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
