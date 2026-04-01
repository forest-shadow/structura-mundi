---
aliases:
  - The Network Edge
note_type: overview
area: computer-science
domain: networking
section: internet
parent: "[[Internet]]"
status: seed
related:
  - "[[Internet]]"
  - "[[TCP IP Model]]"
  - "[[Client-Server Model]]"
  - "[[End System]]"
  - "[[Access Network]]"
tags: []
---

# Network Edge

## Краткое определение области

`Network Edge` — это обзорная заметка о граничной зоне Internet, где расположены оконечные системы и сети доступа, связывающие эти системы с более широкой межсетевой средой.

## Что входит в эту тему

- `[[End System]]`
- `[[Access Network]]`

## Как устроена ветка

- `End System` фиксирует сами hosts, на которых запускаются приложения и где возникают или потребляются сообщения.
- `Access Network` описывает last-hop инфраструктуру, через которую end systems получают подключение к Internet.
- Более глубокие device-level и protocol-level детали пока не выносятся в отдельные заметки, чтобы ветка не росла раньше времени.

## Рекомендуемый маршрут чтения

1. Сначала зафиксировать `[[End System]]` как базовое понятие про hosts на границе сети.
2. Затем перейти к `[[Access Network]]`, чтобы увидеть, как эти hosts подключаются к Internet.
3. После этого сопоставить ветку с `[[TCP IP Model]]` и `[[Client-Server Model]]`, чтобы развести инфраструктурную и role-centric оптики.

## Соседние overview-ветки

- Родительская рамка: `[[Internet]]`
- Смежная role-centric рамка: `[[Client-Server Model]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен `Network Core` как sibling-узел
- [ ] Проверить, нужен ли отдельный article про `Physical Media` именно внутри Internet-ветки
- [ ] Проверить `related`
