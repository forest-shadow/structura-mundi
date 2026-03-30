---
aliases:
  - Virtual Private Network
note_type: overview
area: computer-science
domain: networking
section: network-security
parent: "[[Network Security]]"
status: seed
related:
  - "[[Network Security]]"
  - "[[Remote Access VPN]]"
  - "[[Site-to-Site VPN]]"
  - "[[VPN Tunneling]]"
  - "[[VPN Protocol Families]]"
tags: []
---

# VPN

## Краткое определение области

`VPN` — это обзорная заметка о Virtual Private Network как способе построить защищенный логический канал поверх общей или недоверенной сети. Вокруг этой темы естественно собираются deployment patterns, tunnel mechanics и protocol families.

## Что входит в эту тему

- `[[Remote Access VPN]]`
- `[[Site-to-Site VPN]]`
- `[[VPN Tunneling]]`
- `[[VPN Protocol Families]]`

## Как устроена ветка

- `Remote Access VPN` описывает защищенный доступ отдельных пользователей или клиентских устройств к удаленной сети.
- `Site-to-Site VPN` фиксирует сценарий соединения двух сетевых сегментов или площадок.
- `VPN Tunneling` объясняет, как логический защищенный канал строится поверх другой транспортной среды.
- `VPN Protocol Families` удерживает карту основных технологических семейств, не заставляя сразу разносить каждое в отдельную note.

## Рекомендуемый маршрут чтения

1. Начать с `[[VPN Tunneling]]`, чтобы понять базовую механику канала.
2. Затем сопоставить `[[Remote Access VPN]]` и `[[Site-to-Site VPN]]`.
3. После этого перейти к `[[VPN Protocol Families]]`.
4. Затем вернуть тему в более широкую рамку `[[Network Security]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Network Security]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про `IPsec VPN`, `SSL VPN`, `OpenVPN` и `WireGuard`
- [ ] Проверить границу между `VPN` и более широкими access-моделями
- [ ] Проверить `related`
