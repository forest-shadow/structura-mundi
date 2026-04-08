---
aliases:
  - Origin
note_type: article
area: computer-science
domain: web-platform
section: web-origin-model
parent: "[[Web Origin Model]]"
status: seed
related:
  - "[[Same-Origin Policy]]"
  - "[[CORS (Cross-Origin Resource Sharing)]]"
tags:
  - web
  - security
---

# Web Origin

## Краткое определение

Каноническая статья про `origin` как базовую единицу идентичности web-ресурса в браузере, от которой зависят same-origin и cross-origin правила.

## Основная идея или механизм

Эта заметка должна объяснять, как origin задаёт границу доверия и почему браузер сравнивает запросы, документы и доступ к данным именно через эту модель.

## Границы темы

- Входит: определение origin и его роль в браузерной модели безопасности.
- Не входит: полный разбор всех разрешающих механизмов вроде `CORS`.

## Связи с другими заметками

Родительская тема:

`[[Web Origin Model]]`

Связанные заметки:

- `[[Same-Origin Policy]]`
- `[[CORS]]`

## Примеры, случаи или следствия

Добавить примеры same-origin и cross-origin сценариев для разных URL.

## Что стоит раскрыть дальше

- [ ] Уточнить определение origin
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
