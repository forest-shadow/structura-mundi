---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Service Mesh]]"
status: seed
related:
  - "[[Service Mesh Data Plane]]"
  - "[[Service Endpoint]]"
  - "[[Proxy]]"
tags: []
---

# Service Mesh Control Plane

## Краткое определение

`Service Mesh Control Plane` — это управляющий слой service mesh, который распространяет конфигурацию, политики и сетевые правила на прокси и другие компоненты data plane.

## Основная идея или механизм

Нужно раскрыть, как control plane централизует policy distribution, service discovery, traffic rules и security configuration, не обрабатывая пользовательский трафик непосредственно в datapath.

## Границы темы

- Что относится к control plane как к слою управления.
- Чем control plane отличается от data plane и от generic orchestration layer.

## Связи с другими заметками

Родительская тема:

`[[Service Mesh]]`

Связанные заметки:

- `[[Service Mesh Data Plane]]`
- `[[Service Endpoint]]`
- `[[Proxy]]`

## Примеры, случаи или следствия

Добавить 1-3 примера policy propagation, route configuration и управления сертификатами.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
