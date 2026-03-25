---
aliases:
  - Domain Name System
note_type: article
area: computer-science
domain: networking
section: internet
parent: "[[Internet]]"
status: seed
related:
  - "[[Internet]]"
  - "[[IP Addressing]]"
  - "[[TCP IP Application Layer]]"
tags: []
---

# DNS

## Краткое определение

`DNS` — это статья о распределенной системе именования, которая связывает доменные имена с сетевыми адресами и делает Internet пригодной для человечески удобной навигации.

## Границы темы

- Входит: DNS как distributed naming layer в Internet.
- Не входит: полный operational разбор zone administration и DNS security extensions.

## Связи с другими заметками

Родительская тема:

`[[Internet]]`

Связанные заметки:

- `[[IP Addressing]]`
- `[[Routing]]`
- `[[TCP IP Application Layer]]`

## Примеры, случаи или следствия

- DNS позволяет работать с именами, а не с числовыми IP-адресами напрямую.
- Отказ DNS не выключает адресацию как таковую, но делает сеть менее пригодной для практического использования.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Recursive Resolver` и `Authoritative DNS Server`
- [ ] Проверить `related`
