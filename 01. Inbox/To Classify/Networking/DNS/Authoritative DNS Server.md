---
aliases:
  - Authoritative Name Server
note_type: article
area: computer-science
domain: networking
section: dns
parent: "[[DNS]]"
status: seed
related:
  - "[[DNS]]"
  - "[[DNS Resolution]]"
  - "[[Recursive Resolver]]"
  - "[[DNS Zone]]"
tags: []
---

# Authoritative DNS Server

## Краткое определение

`Authoritative DNS Server` — это DNS-сервер, который хранит и выдает авторитетные данные для определенной зоны, а не просто пересылает или кэширует ответы.

## Основная идея или механизм

Авторитативный сервер отвечает за конкретную часть пространства имен. Он возвращает записи, которыми реально управляет, и тем самым выступает источником истины для своей зоны.

## Границы темы

- Входит: роль authoritative-сервера в DNS, связь с зонами и отличие от recursive resolver.
- Не входит: полный operational разбор администрирования production DNS-инфраструктуры.

## Связи с другими заметками

Родительская тема:

`[[DNS]]`

Связанные заметки:

- `[[DNS Resolution]]`
- `[[Recursive Resolver]]`
- `[[DNS Zone]]`

## Примеры, случаи или следствия

- Для домена ответы о записях возвращаются именно authoritative-серверами соответствующей зоны.
- Делегирование в DNS означает, что authoritative-ответственность передается вниз по иерархии пространства имен.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные статьи про `Root Name Server` и `TLD Name Server`
- [ ] Решить, когда нужен отдельный article про `Zone Transfer`
- [ ] Проверить `related`
