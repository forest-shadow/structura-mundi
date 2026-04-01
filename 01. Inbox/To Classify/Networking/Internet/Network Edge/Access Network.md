---
aliases:
  - Access Networks
note_type: article
area: computer-science
domain: networking
section: internet
parent: "[[Network Edge]]"
status: seed
related:
  - "[[Network Edge]]"
  - "[[End System]]"
  - "[[TCP IP Link Layer]]"
  - "[[Network Topology]]"
tags: []
---

# Access Network

## Краткое определение

`Access Network` — это сеть доступа, которая соединяет end system с более широкой Internet-инфраструктурой и образует last-hop или first-hop участок сетевого пути.

## Основная идея или механизм

Сеть доступа определяет, каким образом host получает физическое и логическое подключение к Internet: через Ethernet, Wi-Fi, cable access, DSL, fiber, cellular network или другие технологии доступа. Она не равна самому Internet core, а обслуживает вход и выход оконечных систем в межсетевую среду.

## Границы темы

- Входит: last-hop connectivity между host и остальной сетью.
- Не входит: глобальная маршрутизация Internet в целом.
- Не входит: сам host как конечная система; это тема `[[End System]]`.

## Связи с другими заметками

Родительская тема:

`[[Network Edge]]`

Связанные заметки:

- `[[End System]]`
- `[[TCP IP Link Layer]]`
- `[[Network Topology]]`

## Примеры, случаи или следствия

- Домашняя Wi-Fi сеть и провайдерский last-mile сегмент образуют типичный пример access network.
- Разница между wired и wireless access влияет на latency, bandwidth и packet loss, хотя host и прикладной протокол могут оставаться теми же.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Home Network`, `Enterprise Access Network` и `Mobile Access Network`
- [ ] Проверить, нужен ли отдельный article про `Last-Mile Connectivity`
- [ ] Проверить `related`
