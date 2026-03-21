---
aliases: []
note_type: article
area: computer-science
domain: web-platform
section: cors
parent: "[[CORS]]"
status: seed
related:
  - "[[CORS Response Headers]]"
  - "[[Same-Origin Policy]]"
tags:
  - web
  - security
---

# Credentialed CORS Requests

## Краткое определение

Каноническая статья про cross-origin запросы с credentials, для которых браузер и сервер применяют более строгие правила согласования.

## Основная идея или механизм

Эта заметка должна объяснять, как cookies, authorization data и credentials mode меняют поведение CORS и почему такие запросы нельзя разрешать теми же правилами, что и анонимные.

## Границы темы

- Входит: credentialed cross-origin requests и их ограничения.
- Не входит: все аспекты аутентификации и авторизации вне CORS.

## Связи с другими заметками

Родительская тема:

`[[CORS]]`

Связанные заметки:

- `[[CORS Response Headers]]`
- `[[Same-Origin Policy]]`

## Примеры, случаи или следствия

Добавить примеры ошибок конфигурации при сочетании credentials и wildcard origin.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
