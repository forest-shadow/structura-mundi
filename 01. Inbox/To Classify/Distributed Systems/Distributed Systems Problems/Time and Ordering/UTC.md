---
aliases:
  - Coordinated Universal Time
  - Координированное всемирное время
note_type: article
area: computer-science
domain: distributed-systems
section: distributed-systems-problems
parent: "[[Time and Ordering]]"
status: seed
related:
  - "[[Time and Ordering]]"
  - "[[Distributed Systems Problems]]"
  - "[[Clock Synchronization]]"
  - "[[Coordination and Consensus]]"
tags: []
---

# UTC

## Краткое определение

`UTC` - это общая reference-scale времени, относительно которой в распределенных системах интерпретируются wall-clock timestamps разных узлов. Она нужна как внешняя точка отсчета, но не устраняет сама по себе сетевые задержки, drift и рассогласование локальных часов.

## Основная идея или механизм

`UTC` дает системам общий язык для выражения времени: меток событий, сроков действия токенов, TTL, lease interval boundaries и окон валидности сертификатов. Практическая проблема состоит в том, что каждый узел знает `UTC` только через приближение, получаемое через локальные часы и механизмы синхронизации.

## Границы темы

- В тему входит `UTC` как внешняя временная шкала и reference point для физических часов.
- Рядом, но не совпадает с ней, находятся local time, time zones, daylight saving rules и purely logical clocks.

## Связи с другими заметками

Родительская тема:

- `[[Time and Ordering]]`

Связанные заметки:

- `[[Clock Synchronization]]`
- `[[Coordination and Consensus]]`
- `[[Distributed Systems Problems]]`

## Примеры, случаи или следствия

- Сопоставление логов между несколькими сервисами имеет смысл только если их локальные часы достаточно близки к общей шкале вроде `UTC`.
- Срок действия JWT, TLS certificate validity window и lease-based coordination опираются на приближение к одному и тому же внешнему времени.
- Даже если два узла пишут timestamps в `UTC`, это ещё не гарантирует корректный causal order событий.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между `UTC`, Unix time и local time representation
- [ ] Добавить примеры operational-ошибок из-за clock skew
- [ ] Проверить `aliases`
- [ ] Проверить `related`
