---
aliases:
  - TLS Offload
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[TLS]]"
status: seed
related:
  - "[[TLS]]"
  - "[[TLS Handshake]]"
  - "[[Reverse Proxy]]"
  - "[[Layer 7 Proxy]]"
  - "[[Service Mesh]]"
  - "[[HTTP]]"
tags: []
---

# TLS Termination

## Краткое определение

`TLS Termination` — это завершение TLS-соединения на промежуточном сетевом узле, который принимает защищенное соединение от клиента и уже дальше взаимодействует с upstream-системами по своей внутренней схеме.

## Основная идея или механизм

Промежуточный узел берет на себя криптографическое завершение внешнего TLS-сеанса. Это позволяет централизовать certificate handling, policy enforcement, traffic inspection и другие функции на boundary-узле, не перенося их одинаково на каждый origin-service.

## Границы темы

- Входит: завершение TLS на intermediary node и его архитектурные последствия.
- Не входит: весь reverse proxying как таковой; `Reverse Proxy` — более широкая тема.

## Связи с другими заметками

Родительская тема:

`[[TLS]]`

Связанные заметки:

- `[[TLS Handshake]]`
- `[[Reverse Proxy]]`
- `[[Layer 7 Proxy]]`
- `[[Service Mesh]]`
- `[[HTTP]]`

## Примеры, случаи или следствия

- Reverse proxy может выступать точкой TLS termination перед backend-инстансами.
- Вынос TLS termination на boundary node упрощает operational control, но меняет trust model внутри системы.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли рядом отдельный article про `TLS Passthrough`
- [ ] Проверить границу между termination и end-to-end encryption
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
