---
aliases: []
note_type: article
area: computer-science
domain: networking
section: packet-switches
parent: "[[Packet Switches]]"
status: seed
related:
  - "[[Routing]]"
  - "[[IP Addressing]]"
  - "[[Network Layer]]"
  - "[[Packet Switches]]"
tags: []
---

# Router

## Краткое определение

`Router` — это статья про сетевое устройство, которое пересылает пакеты между различными сетями, используя network-layer адресацию и таблицы пересылки для выбора next hop.

## Основная идея или механизм

`Router` работает на границе сетей и принимает решение не просто о том, в какой локальный порт отправить кадр, а о том, через какой следующий узел или интерфейс пакет должен двигаться дальше к целевой сети. Поэтому router тесно связан с адресацией, маршрутами и network-layer логикой.

## Границы темы

- Входит: router как forwarding device, связь с next hop, forwarding table и межсетевой пересылкой.
- Не входит: полный разбор всех routing protocols, vendor-specific implementations и composite home gateway features.

## Связи с другими заметками

Родительская тема:

`[[Packet Switches]]`

Связанные заметки:

- `[[Routing]]`
- `[[IP Addressing]]`
- `[[Network Layer]]`
- `[[Packet Switches]]`

## Примеры, случаи или следствия

Router полезно понимать как устройство, которое соединяет отдельные IP-сети: домашняя сеть и сеть провайдера, офисные сегменты или автономные сети в более крупной инфраструктуре. Именно через routers логическая адресация превращается в достижимый путь между сетями.

## Что стоит раскрыть дальше

- [ ] Добавить связь между `Router` и `Forwarding Table`
- [ ] Уточнить границу между `Router` и `Routing`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
