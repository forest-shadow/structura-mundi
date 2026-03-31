---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Roles]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Proxy Roles]]"
  - "[[Forward Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[Layer 7 Proxy]]"
  - "[[TLS Termination]]"
  - "[[Origin Shielding]]"
  - "[[CDN and Edge Cache]]"
tags: []
---

# Reverse Proxy

## Краткое определение

`Reverse Proxy` — это прокси, который действует со стороны сервера: внешний клиент обращается к прокси как к публичной точке входа, а тот уже пересылает запрос одному или нескольким внутренним origin-сервисам.

## Основная идея или механизм

Reverse proxy принимает входящий трафик, скрывает внутреннюю топологию backend-системы и берет на себя часть инфраструктурных функций вокруг origin-сервисов. Часто именно здесь размещаются request routing, caching, security policy, а также соседние механизмы вроде `TLS Termination`.

## Границы темы

- Входит: server-side proxying, публикация внутренних сервисов наружу, защита и распределение входящего трафика.
- Не входит: клиентский контроль исходящего доступа; это уже тема `Forward Proxy`.
- Не входит как самостоятельные широкие темы: `TLS Termination` и `Origin Shielding`; они связаны с reverse proxy, но не исчерпываются им.

## Связи с другими заметками

Родительская тема:

`[[Proxy Roles]]`

Связанные заметки:

- `[[Forward Proxy]]`
- `[[HTTP Proxy]]`
- `[[Layer 7 Proxy]]`
- `[[TLS Termination]]`
- `[[Origin Shielding]]`
- `[[CDN and Edge Cache]]`

## Примеры, случаи или следствия

- Reverse proxy может быть публичной точкой входа перед группой backend-инстансов.
- Через reverse proxy удобно централизованно применять routing, caching и security policy перед origin.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужен отдельный article про `Ingress Proxy`
- [ ] Проверить границу между `Reverse Proxy`, `Load Balancer` и `API Gateway`
- [ ] Проверить `related`
