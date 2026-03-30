---
aliases:
  - Gateway-to-Gateway VPN
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[VPN]]"
status: draft
related:
  - "[[VPN]]"
  - "[[Remote Access VPN]]"
  - "[[VPN Tunneling]]"
  - "[[VPN Protocol Families]]"
tags: []
---

# Site-to-Site VPN

## Краткое определение

`Site-to-Site VPN` — это статья о сценарии, в котором защищенный логический канал строится между двумя сетевыми сегментами, площадками или gateway-узлами, а не между отдельным пользователем и целевой сетью.

## Основная идея или механизм

Суть `Site-to-Site VPN` в том, что две сети связываются через защищенный tunnel, так что узлы по обе стороны могут обмениваться трафиком как между частями единой логической инфраструктуры.

## Границы темы

- Входит: network-to-network connectivity, branch interconnect, защищенная связность между площадками.
- Не входит: персональный удаленный доступ отдельного клиента как в `Remote Access VPN`.

## Связи с другими заметками

Родительская тема:

`[[VPN]]`

Связанные заметки:

- `[[Remote Access VPN]]`
- `[[VPN Tunneling]]`
- `[[VPN Protocol Families]]`

## Примеры, случаи или следствия

- Соединение головного офиса и филиала поверх публичной сети.
- Связность между on-premise сегментом и облачным приватным окружением.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между static и dynamic site connectivity
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
