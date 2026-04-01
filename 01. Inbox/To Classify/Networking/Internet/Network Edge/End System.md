---
aliases:
  - End Host
  - Host
note_type: article
area: computer-science
domain: networking
section: internet
parent: "[[Network Edge]]"
status: seed
related:
  - "[[Network Edge]]"
  - "[[Internet]]"
  - "[[Access Network]]"
  - "[[Client-Server Model]]"
  - "[[Server Host]]"
tags: []
---

# End System

## Краткое определение

`End System` — это host на границе сети, на котором исполняются приложения и который выступает конечной точкой отправки или получения данных в Internet.

## Основная идея или механизм

Именно end systems порождают прикладной трафик и потребляют результаты сетевого обмена. В эту категорию входят desktops, laptops, smartphones, servers, tablets, IoT devices и другие вычислительные узлы, которые используют сетевой стек для общения с удаленными системами.

## Границы темы

- Входит: host как конечная вычислительная система на network edge.
- Не входит: подробная роль `server` или `client` как архитектурных позиций внутри `[[Client-Server Model]]`.
- Не входит: last-hop инфраструктура подключения, которая относится к `[[Access Network]]`.

## Связи с другими заметками

Родительская тема:

`[[Network Edge]]`

Связанные заметки:

- `[[Access Network]]`
- `[[Client-Server Model]]`
- `[[Server Host]]`

## Примеры, случаи или следствия

- Смартфон, открывающий веб-страницу, является end system, потому что именно на нем инициируется и принимается прикладной обмен.
- Сервер тоже остается end system, хотя одновременно может играть роль `server` в client-server архитектуре.
- Один и тот же host может выступать клиентом, сервером или peer в зависимости от конкретной модели взаимодействия.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Socket Interface`
- [ ] Проверить, когда рядом нужны `Process-to-Process Communication` и ports
- [ ] Проверить `related`
