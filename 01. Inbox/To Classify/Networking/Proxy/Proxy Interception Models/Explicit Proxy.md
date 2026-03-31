---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Interception Models]]"
status: seed
related:
  - "[[Proxy Interception Models]]"
  - "[[Forward Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[SOCKS Proxy]]"
tags: []
---

# Explicit Proxy

## Краткое определение

`Explicit Proxy` — это прокси, который используется по явной настройке клиента или приложения.

## Основная идея или механизм

Клиент заранее знает адрес прокси и отправляет трафик именно ему. Это делает посредничество явной частью клиентской конфигурации и хорошо сочетается с policy-driven outbound access.

## Границы темы

- Входит: явная proxy-configuration со стороны клиента.
- Не входит: скрытый сетевой перехват трафика; это уже `Transparent Proxy` или `Intercepting Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Interception Models]]`

Связанные заметки:

- `[[Forward Proxy]]`
- `[[HTTP Proxy]]`
- `[[SOCKS Proxy]]`

## Примеры, случаи или следствия

- Браузер может быть настроен использовать explicit HTTP proxy.
- Корпоративный клиент может быть явно привязан к определенному outbound proxy.

## Что стоит раскрыть дальше

- [ ] Проверить `related`
