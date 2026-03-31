---
aliases:
  - Explicit Client Proxy
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Roles]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Proxy Roles]]"
  - "[[Reverse Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[SOCKS Proxy]]"
  - "[[Proxy Authentication]]"
tags: []
---

# Forward Proxy

## Краткое определение

`Forward Proxy` — это прокси, который действует со стороны клиента: клиент отправляет запрос посреднику, а тот уже обращается к внешнему ресурсу от имени клиента.

## Основная идея или механизм

Forward proxy контролирует исходящий доступ клиента во внешнюю сеть. Он может скрывать адрес клиента, применять access policy, журналировать запросы, фильтровать контент и в некоторых сценариях кэшировать ответы.

## Границы темы

- Входит: client-side proxying, egress control, policy enforcement, посредничество между клиентом и внешним сервером.
- Не входит: публикация внутренних сервисов наружу и обработка входящего server-side трафика; это относится к `Reverse Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Roles]]`

Связанные заметки:

- `[[Reverse Proxy]]`
- `[[HTTP Proxy]]`
- `[[SOCKS Proxy]]`
- `[[Proxy Authentication]]`

## Примеры, случаи или следствия

- Корпоративный web proxy может ограничивать доступ пользователей к внешним ресурсам.
- Клиент может использовать forward proxy для маршрутизации запросов через контролируемую сетевую точку выхода.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Egress Proxy`
- [ ] Проверить `related`
