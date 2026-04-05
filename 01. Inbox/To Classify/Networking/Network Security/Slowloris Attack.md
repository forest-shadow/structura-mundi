---
aliases:
  - Slow HTTP Attack
  - Атака Slowloris
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[Network Security]]"
status: seed
related:
  - "[[Network Security]]"
  - "[[HTTP]]"
  - "[[Timeouts and Cancellation]]"
  - "[[Server Resource Management]]"
  - "[[Go Servers]]"
tags: []
---

# Slowloris Attack

## Краткое определение

`Slowloris Attack` — это атака отказа в обслуживании, при которой атакующий удерживает большое число HTTP-соединений открытыми, отправляя запросы чрезвычайно медленно и не давая серверу вовремя освободить ресурсы.

## Основная идея или механизм

Нужно раскрыть, как неполные заголовки, долго живущие соединения и слабые серверные лимиты позволяют истощать connection slots, worker time или memory без большого объема трафика.

## Границы темы

- Входит: медленная отправка заголовков, удержание соединений, истощение concurrency budget сервера.
- Не входит: любые volumetric DDoS-атаки и не любой HTTP flood.

## Связи с другими заметками

Родительская тема:

`[[Network Security]]`

Связанные заметки:

- `[[HTTP]]`
- `[[Timeouts and Cancellation]]`
- `[[Server Resource Management]]`
- `[[Go Servers]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария, где отсутствие `read header timeout`, слабые лимиты keep-alive или неудачная модель worker allocation делают сервер уязвимым для Slowloris.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи с server-side mitigation notes
- [ ] Проверить `aliases`
- [ ] Проверить `related`
- [ ] Проверить `tags`
