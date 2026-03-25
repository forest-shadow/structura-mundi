---
aliases: []
note_type: article
area: computer-science
domain: networking
section: internet
parent: "[[Internet]]"
status: seed
related:
  - "[[Internet]]"
  - "[[IP Addressing]]"
  - "[[TCP IP Internet Layer]]"
tags: []
---

# Routing

## Краткое определение

`Routing` — это статья о том, как в Internet выбираются пути доставки пакетов между сетями и как логическая адресация превращается в достижимый маршрут.

## Границы темы

- Входит: routing как механизм выбора пути между сетями.
- Не входит: полный разбор всех routing protocols и vendor-specific implementations.

## Связи с другими заметками

Родительская тема:

`[[Internet]]`

Связанные заметки:

- `[[IP Addressing]]`
- `[[TCP IP Internet Layer]]`
- `[[DNS]]`

## Примеры, случаи или следствия

- Адрес сам по себе не гарантирует доставку: нужен механизм выбора next hop и пути.
- Масштабируемость Internet зависит от того, что routing работает между множеством автономных сетей, а не внутри одной локальной topology.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Router`, `Autonomous System` и `BGP`
- [ ] Проверить `related`
