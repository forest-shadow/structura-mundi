---
aliases:
  - dns-prefetch
note_type: article
area: computer-science
domain: web-platform
section: resource-hints
parent: "[[Resource Hints]]"
status: seed
related:
  - "[[Preconnect]]"
tags:
  - web
  - performance
---

# DNS Prefetch

## Краткое определение

Каноническая статья про `dns-prefetch`, которым браузеру подсказывают заранее разрешить DNS-имя внешнего источника.

## Основная идея или механизм

`DNS Prefetch` помогает заранее выполнить только DNS lookup. Это более лёгкий и менее дорогой hint, чем `preconnect`.

## Границы темы

- Входит: назначение и поведение `dns-prefetch`.
- Не входит: полный разбор всех connection-warming стратегий.

## Связи с другими заметками

Родительская тема:

`[[Resource Hints]]`

Связанные заметки:

- `[[Preconnect]]`

## Примеры, случаи или следствия

Полезен, когда есть внешний хост, к которому браузер, вероятно, скоро обратится, но полный прогрев соединения пока избыточен.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между `dns-prefetch` и `preconnect`
- [ ] Добавить примеры для third-party origins
- [ ] Проверить `aliases`
