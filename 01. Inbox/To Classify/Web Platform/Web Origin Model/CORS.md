---
aliases:
  - Cross-Origin Resource Sharing
note_type: article
area: computer-science
domain: web-platform
section: web-origin-model
parent: "[[Web Origin Model]]"
status: seed
related:
  - "[[Web Origin]]"
  - "[[Same-Origin Policy]]"
tags:
  - web
  - security
---

# CORS

## Краткое определение

Каноническая статья про `CORS` как механизм контролируемого cross-origin доступа, который работает поверх `same-origin policy`, а не вместо неё.

## Основная идея или механизм

`CORS` описывает согласование между браузером и сервером о том, можно ли читать ответ на cross-origin запрос.

- Браузер отправляет `Origin`, чтобы сообщить серверу источник запроса.
- Для части запросов браузер сначала делает предварительный `OPTIONS`-запрос, чтобы проверить допустимые методы и заголовки.
- Сервер отвечает access-control response headers и тем самым либо разрешает чтение ответа, либо оставляет его заблокированным.
- Если запрос идёт с credentials, правила становятся строже: нельзя использовать те же упрощённые настройки, что и для анонимного доступа.

## Границы темы

- Входит: общая модель CORS, preflight, request/response headers и особенности credentialed cross-origin requests.
- Не входит: общая теория аутентификации, cookies вне контекста CORS и полный разбор broader browser security.

## Связи с другими заметками

Родительская тема:

`[[Web Origin Model]]`

Связанные заметки:

- `[[Web Origin]]`
- `[[Same-Origin Policy]]`

## Примеры, случаи или следствия

- `GET`-запрос с `Origin` может быть разрешён без preflight, если сервер вернёт корректный `Access-Control-Allow-Origin`.
- `PATCH`-запрос с нестандартным заголовком обычно потребует preflight перед основным запросом.
- Конфигурация `Access-Control-Allow-Credentials: true` вместе с wildcard origin приводит к ошибочной CORS-настройке.

## Что стоит раскрыть дальше

- [ ] Уточнить терминологию вокруг simple и preflighted requests
- [ ] Добавить короткую схему полного browser/server обмена
- [ ] Проверить, нужен ли позже отдельный узел про preflight как самостоятельный механизм
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
