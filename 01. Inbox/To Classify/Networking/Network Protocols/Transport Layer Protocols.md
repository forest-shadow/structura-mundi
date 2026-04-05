---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-protocols
parent: "[[Network Protocols]]"
status: seed
related:
  - "[[Network Protocols]]"
  - "[[TCP IP Transport Layer]]"
  - "[[Transport Layer]]"
  - "[[QUIC]]"
tags: []
---

# Transport Layer Protocols

## Краткое определение области

`Transport Layer Protocols` — это обзорная заметка о протоколах, которые обеспечивают end-to-end обмен данными между прикладными процессами поверх сетевой адресации.

## Что входит в эту тему

- Общая роль transport protocols в сетевом стеке.
- Различие между доставкой между хостами и взаимодействием между прикладными процессами.
- Связь с `[[TCP IP Transport Layer]]` и `[[Transport Layer]]`.
- `[[QUIC]]` как современный transport-level protocol поверх UDP.

## Как устроена ветка

- `QUIC` уже стоит держать как отдельную child-статью, потому что он важен не только как еще один transport protocol, но и как точка пересечения transport semantics, modern web delivery и TLS-integrated connection establishment.
- `TCP` и `UDP` стоит выносить рядом позже, когда появятся более плотные сравнения, use cases и trade-offs.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `QUIC`, `TCP` и `UDP`
- [ ] Проверить границу между `QUIC` и `HTTP/3`
- [ ] Решить, когда нужны `TCP` и `UDP`
- [ ] Проверить `related`
