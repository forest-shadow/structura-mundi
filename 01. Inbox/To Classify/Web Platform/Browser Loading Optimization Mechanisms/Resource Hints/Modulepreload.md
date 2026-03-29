---
aliases:
  - modulepreload
note_type: article
area: computer-science
domain: web-platform
section: resource-hints
parent: "[[Resource Hints]]"
status: seed
related:
  - "[[Preload]]"
  - "[[Fetch Priority]]"
tags:
  - web
  - performance
---

# Modulepreload

## Краткое определение

Каноническая статья про механизм `modulepreload`, через который браузеру заранее подсказывают загрузить JavaScript-модули, нужные текущей странице.

## Основная идея или механизм

`Modulepreload` можно понимать как специализированный вариант ранней загрузки для мира ES modules. Он стоит рядом с `preload`, но не сводится к простому переименованию, потому что учитывает особенности модульной загрузки.

## Границы темы

- Входит: назначение и поведение `modulepreload`.
- Не входит: полный разбор module scripts в целом.

## Связи с другими заметками

Родительская тема:

`[[Resource Hints]]`

Связанные заметки:

- `[[Preload]]`
- `[[Fetch Priority]]`

## Примеры, случаи или следствия

Полезен для ускорения старта модульных приложений, когда важно раньше начать загрузку JavaScript module graph.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между `preload` и `modulepreload`
- [ ] Добавить примеры для entry module
- [ ] Проверить `aliases`
