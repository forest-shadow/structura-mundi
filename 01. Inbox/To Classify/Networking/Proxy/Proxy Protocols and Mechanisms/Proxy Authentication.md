---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Protocols and Mechanisms]]"
status: seed
related:
  - "[[Forward Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[Proxy Protocols and Mechanisms]]"
tags: []
---

# Proxy Authentication

## Краткое определение

`Proxy Authentication` — это механизм аутентификации клиента перед прокси-узлом, а не перед конечным origin-сервисом.

## Основная идея или механизм

Прокси как отдельный intermediary node может требовать собственной аутентификации, чтобы контролировать доступ к своим функциям и к сетевому пути через себя.

## Границы темы

- Входит: authentication at the proxy boundary.
- Не входит: origin-server authentication как часть application protocol с целевым сервисом.

## Связи с другими заметками

Родительская тема:

`[[Proxy Protocols and Mechanisms]]`

Связанные заметки:

- `[[Forward Proxy]]`
- `[[HTTP Proxy]]`

## Примеры, случаи или следствия

- Корпоративный proxy может требовать отдельную аутентификацию пользователей перед выдачей доступа во внешнюю сеть.
- Наличие proxy-authentication делает trust boundary прокси явной частью архитектуры.

## Что стоит раскрыть дальше

- [ ] Проверить `related`
