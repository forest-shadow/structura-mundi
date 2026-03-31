---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Forward Proxy]]"
  - "[[Reverse Proxy]]"
  - "[[HTTP Proxy]]"
  - "[[TLS Termination]]"
  - "[[Origin Shielding]]"
tags: []
---

# Proxy Functions

## Краткое определение

`Proxy Functions` — это статья о типовых функциях, которые прокси может брать на себя в сетевой архитектуре.

## Основная идея или механизм

Прокси важен не только как отдельный тип узла, но и как место концентрации operational функций вокруг проходящего трафика. При этом не все такие функции должны сразу становиться отдельными каноническими notes: часть из них пока лучше удерживать в одной рамке.

## Границы темы

- Входит: типовые proxy-oriented функции, которые часто группируются вокруг client-side и server-side посредников.
- Не входит как полностью дочерняя часть этой заметки: `TLS Termination` и `Origin Shielding`, потому что это более широкие темы, связанные не только с proxying.

## Ключевые функции

### Proxy Caching

Прокси может кэшировать ответы и снижать нагрузку на upstream/origin. Эта функция особенно важна для HTTP-aware proxying и пересекается с более широкой веткой `[[CDN and Edge Cache]]`.

### Proxy Content Filtering

Прокси может фильтровать трафик по policy, категориям контента, признакам риска или корпоративным правилам доступа.

### Proxy Request Routing

Прокси может определять, куда именно направить запрос дальше, опираясь на host, path, headers, policy или внутреннюю топологию upstream-сервисов.

## Связи с другими заметками

Родительская тема:

`[[Proxy]]`

Связанные заметки:

- `[[Forward Proxy]]`
- `[[Reverse Proxy]]`
- `[[HTTP Proxy]]`
- `[[TLS Termination]]`
- `[[Origin Shielding]]`

## Примеры, случаи или следствия

- Forward proxy чаще концентрирует policy-driven filtering и outbound access control.
- Reverse proxy чаще концентрирует request routing и proxy-side caching перед origin.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Proxy Caching`
- [ ] Решить, когда нужен отдельный article про `Proxy Content Filtering`
- [ ] Решить, когда нужен отдельный article про `Proxy Request Routing`
- [ ] Проверить `related`
