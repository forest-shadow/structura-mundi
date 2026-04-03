---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Service Mesh]]"
status: seed
related:
  - "[[Service Mesh Control Plane]]"
  - "[[Layer 7 Proxy]]"
  - "[[TLS Termination]]"
tags: []
---

# Service Mesh Data Plane

## Краткое определение

`Service Mesh Data Plane` — это слой service mesh, через который фактически проходит прикладной трафик между сервисами и в котором применяются маршрутизация, security policy и observability hooks.

## Основная идея или механизм

Нужно раскрыть, как data plane перехватывает и обрабатывает service-to-service traffic, почему он отделен от control plane и какую роль играют proxy-компоненты в этом слое.

## Границы темы

- Что относится к data plane как к пути прохождения трафика.
- Чем data plane отличается от control plane и от обычного standalone reverse proxy.

## Связи с другими заметками

Родительская тема:

`[[Service Mesh]]`

Связанные заметки:

- `[[Service Mesh Control Plane]]`
- `[[Layer 7 Proxy]]`
- `[[TLS Termination]]`

## Примеры, случаи или следствия

Добавить 1-3 примера traffic interception, mTLS enforcement и сбора телеметрии в datapath.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
