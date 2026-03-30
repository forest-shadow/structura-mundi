---
aliases:
  - Client-to-Site VPN
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[VPN]]"
status: draft
related:
  - "[[VPN]]"
  - "[[Site-to-Site VPN]]"
  - "[[VPN Tunneling]]"
  - "[[VPN Protocol Families]]"
tags: []
---

# Remote Access VPN

## Краткое определение

`Remote Access VPN` — это статья о сценарии, в котором отдельный пользователь или клиентское устройство получает защищенный доступ к удаленной частной сети через недоверенную внешнюю среду, чаще всего Internet.

## Основная идея или механизм

Суть `Remote Access VPN` в том, что клиент устанавливает защищенный tunnel до gateway или concentrator и получает логический доступ к внутренним ресурсам так, как если бы находился внутри целевой сети.

## Границы темы

- Входит: user-to-network access pattern, client connectivity, удаленный вход в частную сеть.
- Не входит: соединение двух целых сетевых площадок как в `Site-to-Site VPN`.

## Связи с другими заметками

Родительская тема:

`[[VPN]]`

Связанные заметки:

- `[[Site-to-Site VPN]]`
- `[[VPN Tunneling]]`
- `[[VPN Protocol Families]]`

## Примеры, случаи или следствия

- Доступ сотрудника к корпоративной сети из домашней или публичной среды.
- Подключение администратора к приватному operational perimeter удаленного окружения.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между full-tunnel и split-tunnel access
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
