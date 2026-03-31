---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Networking]]"
status: seed
related:
  - "[[Reverse Proxy]]"
  - "[[Layer 7 Proxy]]"
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

`[[Networking]]`

Связанные заметки:

- `[[Reverse Proxy]]`
- `[[Layer 7 Proxy]]`
- `[[HTTP]]`

## Примеры, случаи или следствия

- Reverse proxy может выступать точкой TLS termination перед backend-инстансами.
- Вынос TLS termination на boundary node упрощает operational control, но меняет trust model внутри системы.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли рядом отдельный article про `TLS Passthrough`
- [ ] Проверить `related`
