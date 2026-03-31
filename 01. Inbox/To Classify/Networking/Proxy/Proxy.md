---
aliases:
  - Proxy Server
note_type: overview
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[Proxy Roles]]"
  - "[[Proxy Interception Models]]"
  - "[[Proxy Processing Models]]"
  - "[[Proxy Protocols and Mechanisms]]"
  - "[[Proxy Functions]]"
  - "[[TLS Termination]]"
  - "[[Origin Shielding]]"
tags: []
---

# Proxy

## Краткое определение области

`Proxy` — это обзорная заметка о сетевом посреднике, который принимает трафик от одной стороны взаимодействия и передает его дальше от имени этой стороны или перед ней. Тема охватывает не один конкретный протокол, а общий класс intermediary nodes.

## Что входит в эту тему

- `[[Proxy Roles]]`
- `[[Proxy Interception Models]]`
- `[[Proxy Processing Models]]`
- `[[Proxy Protocols and Mechanisms]]`
- `[[Proxy Functions]]`

## Как устроена ветка

- `Proxy Roles` разделяет прокси по тому, чью сторону они представляют в коммуникации.
- `Proxy Interception Models` фиксирует, как трафик вообще начинает проходить через прокси.
- `Proxy Processing Models` показывает уровень и характер обработки трафика.
- `Proxy Protocols and Mechanisms` удерживает конкретные протокольные и operational mechanisms вроде `HTTP Proxy`, `SOCKS Proxy` и `CONNECT Tunneling`.
- `Proxy Functions` пока остается одной статьей, чтобы не дробить ветку преждевременно.
- Более широкие соседние темы вроде `TLS Termination` и `Origin Shielding` не подчиняются этой ветке, а связываются с ней поперечно.

## Рекомендуемый маршрут чтения

1. Начать с общей рамки `Proxy`.
2. Затем перейти к `[[Proxy Roles]]`, чтобы зафиксировать базовое различие между `Forward Proxy` и `Reverse Proxy`.
3. После этого читать `[[Proxy Interception Models]]` и `[[Proxy Processing Models]]`.
4. Затем перейти к `[[Proxy Protocols and Mechanisms]]`.
5. Завершить `[[Proxy Functions]]`, `[[TLS Termination]]` и `[[Origin Shielding]]` как практическими соседними темами.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Протокольная ветка: `[[Network Protocols]]`
- Прикладная ветка: `[[Application Layer Protocols]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Load Balancer` и `API Gateway`
- [ ] Решить, когда рядом нужен `Service Mesh`
- [ ] Проверить `related`
