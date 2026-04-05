---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-security
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[Network Protocols]]"
  - "[[Internet]]"
  - "[[TLS]]"
  - "[[VPN]]"
tags: []
---

# Network Security

## Краткое определение области

`Network Security` — это обзорная заметка о механизмах защиты сетевого взаимодействия, границ доверия и безопасного доступа поверх недоверенной или общей сетевой среды.

## Что входит в эту тему

- `[[TLS]]`
- `[[VPN]]`
- `Firewall`
- `Network Access Control`
- `Zero Trust Network Access`

## Как устроена ветка

- `TLS` оправдан как отдельный `sub-overview`, потому что тема уже естественно распадается на handshake, certificate validation, mTLS и termination.
- `VPN` уже оправдан как отдельный `sub-overview`, потому что тема быстро распадается на deployment patterns, tunnel mechanics и protocol families.
- Ветка не должна подменять собой всю security-теорию: здесь остаются именно сетевые механизмы, а не общая криптография или identity management.

## Рекомендуемый маршрут чтения

1. Начать с `[[TLS]]`, если нужен protocol-and-trust взгляд на защищенное сетевое соединение.
2. Затем перейти к `[[VPN]]`, если нужен логический защищенный канал поверх недоверенной сети.
3. После этого сопоставить security-оптику с `[[Network Protocols]]` и `[[Internet]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- `[[Network Protocols]]`
- `[[Internet]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Firewall`, `Network Access Control` и `Zero Trust Network Access`
- [ ] Проверить границу между `Network Security` и `Network Protocols`
- [ ] Проверить `related`
