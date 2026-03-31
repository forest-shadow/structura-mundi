---
aliases:
  - Forced Proxy Interception
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy Interception Models]]"
status: seed
related:
  - "[[Proxy Interception Models]]"
  - "[[Transparent Proxy]]"
tags: []
---

# Intercepting Proxy

## Краткое определение

`Intercepting Proxy` — это прокси, к которому трафик перенаправляется принудительно на уровне сети или устройства, а не по явной инициативе клиента.

## Основная идея или механизм

Сеть захватывает трафик и перенаправляет его через прокси-узел с помощью routing policy, NAT, firewall rules или других interception-механизмов. Это делает proxying свойством сетевой инфраструктуры, а не клиентской настройки.

## Границы темы

- Входит: принудительное перенаправление трафика через прокси.
- Не входит: обычный explicit proxy, где клиент сам знает адрес посредника.

## Связи с другими заметками

Родительская тема:

`[[Proxy Interception Models]]`

Связанные заметки:

- `[[Transparent Proxy]]`

## Примеры, случаи или следствия

- Организация может принудительно перенаправлять web traffic через policy-enforcement proxy.
- Intercepting proxying увеличивает управляемость сети, но усложняет модель trust и диагностику маршрута.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли отдельный article про `Captive Portal`
- [ ] Проверить `related`
