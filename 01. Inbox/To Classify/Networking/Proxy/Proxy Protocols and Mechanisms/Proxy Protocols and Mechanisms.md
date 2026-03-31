---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[SOCKS Proxy]]"
  - "[[CONNECT Tunneling]]"
  - "[[Proxy Authentication]]"
  - "[[Proxy Chaining]]"
tags: []
---

# Proxy Protocols and Mechanisms

## Краткое определение области

`Proxy Protocols and Mechanisms` — это обзорная заметка о конкретных протокольных и operational mechanisms, через которые прокси встраивается в сетевое взаимодействие.

## Что входит в эту тему

- `[[HTTP Proxy]]`
- `[[SOCKS Proxy]]`
- `[[CONNECT Tunneling]]`
- `[[Proxy Authentication]]`
- `[[Proxy Chaining]]`

## Как устроена ветка

- `HTTP Proxy` и `SOCKS Proxy` задают два разных канонических семейства proxy-protocol behavior.
- `CONNECT Tunneling` описывает важный механизм туннелирования, особенно в HTTP-context.
- `Proxy Authentication` и `Proxy Chaining` удерживают типовые operational mechanisms вокруг proxy-deployment.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли рядом отдельный article про `Proxy Auto-Configuration`
- [ ] Проверить `related`
