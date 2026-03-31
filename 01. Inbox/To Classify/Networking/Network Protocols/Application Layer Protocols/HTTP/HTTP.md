---
aliases:
  - Hypertext Transfer Protocol
  - HTTP Protocol
  - HTTP Protocols
note_type: overview
area: computer-science
domain: networking
section: network-protocols
parent: "[[Application Layer Protocols]]"
status: seed
related:
  - "[[Application Layer Protocols]]"
  - "[[TCP IP Application Layer]]"
  - "[[HTTP Messages]]"
  - "[[HTTP Methods]]"
  - "[[HTTP Status Codes]]"
  - "[[HTTP Header Fields]]"
  - "[[HTTP Versions]]"
  - "[[Proxy]]"
tags: []
---

# HTTP

## Краткое определение области

`HTTP` — это обзорная заметка о Hypertext Transfer Protocol как прикладном протоколе request-response взаимодействия между клиентами, серверами и промежуточными узлами в Web.

## Что входит в эту тему

- `[[HTTP Messages]]`
- `[[HTTP Methods]]`
- `[[HTTP Status Codes]]`
- `[[HTTP Header Fields]]`
- `[[HTTP Versions]]`
- `[[Proxy]]`

## Как устроена ветка

- `HTTP` служит картой темы и не должен превращаться в одну длинную справочную простыню по всем деталям протокола.
- `HTTP Messages` фиксирует базовую структуру запросов и ответов.
- `HTTP Methods`, `HTTP Status Codes` и `HTTP Header Fields` выделены в отдельные статьи, потому что это самостоятельные устойчивые аспекты HTTP semantics.
- `HTTP Versions` нужна как отдельная статья, чтобы не смешивать protocol semantics с эволюцией transport and framing model от HTTP/1.1 к HTTP/2 и HTTP/3.
- `Proxy` оправдан как вложенный `sub-overview`, потому что HTTP по своей природе включает не только клиента и origin-сервер, но и промежуточные узлы с разными ролями, прежде всего `Forward Proxy` и `Reverse Proxy`.

## Рекомендуемый маршрут чтения

1. Начать с `[[HTTP Messages]]`, чтобы зафиксировать request-response модель.
2. Затем перейти к `[[HTTP Methods]]` и `[[HTTP Status Codes]]`.
3. После этого читать `[[HTTP Header Fields]]`.
4. Затем перейти к `[[Proxy]]`, если нужно увидеть роль промежуточных HTTP-узлов.
5. Завершить `[[HTTP Versions]]`, чтобы понять, как менялась реализация протокола.

## Соседние overview-ветки

- Родительская рамка: `[[Application Layer Protocols]]`
- Соседняя protocol-ветка: `[[DNS]]`
- Соседняя model-ветка: `[[TCP IP Application Layer]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `HTTP Caching`, `Content Negotiation` и `Cookies`
- [ ] Проверить, нужен ли отдельный узел про `HTTP Semantics`
- [ ] Решить, когда рядом с `Proxy` нужны `Load Balancer` и `API Gateway`
- [ ] Проверить `related`
