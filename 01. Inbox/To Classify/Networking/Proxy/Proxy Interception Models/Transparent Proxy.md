---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Interception Models]]"
status: seed
related:
  - "[[Proxy Interception Models]]"
  - "[[Intercepting Proxy]]"
  - "[[Forward Proxy]]"
  - "[[Reverse Proxy]]"
tags: []
---

# Transparent Proxy

## Краткое определение

`Transparent Proxy` — это прокси, через который трафик проходит без явной proxy-настройки на стороне клиента.

## Основная идея или механизм

С точки зрения клиента соединение выглядит прямым или почти прямым, хотя фактически трафик проходит через промежуточный узел. Такая модель важна для сетевых политик, фильтрации и кэширования, но может усложнять диагностику и semantics соединения.

## Границы темы

- Входит: неявное прохождение трафика через посредника.
- Не входит: обычная explicit-конфигурация клиента; это тема `Explicit Proxy`.

## Связи с другими заметками

Родительская тема:

`[[Proxy Interception Models]]`

Связанные заметки:

- `[[Intercepting Proxy]]`
- `[[Forward Proxy]]`
- `[[Reverse Proxy]]`

## Примеры, случаи или следствия

- Сетевой оператор может прозрачно направлять часть трафика через filtering или caching proxy.
- Transparent proxying может ломать ожидания приложений о прямом end-to-end поведении соединения.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `Transparent Proxy` и `Intercepting Proxy`
- [ ] Проверить `related`
