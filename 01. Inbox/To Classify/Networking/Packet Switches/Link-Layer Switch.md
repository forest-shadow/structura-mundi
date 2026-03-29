---
aliases:
  - Layer 2 Switch
  - Ethernet Switch
note_type: article
area: computer-science
domain: networking
section: packet-switches
parent: "[[Packet Switches]]"
status: seed
related:
  - "[[Data Link Layer]]"
  - "[[Link Layer Protocols]]"
  - "[[Packet Switches]]"
  - "[[Router]]"
tags: []
---

# Link-Layer Switch

## Краткое определение

`Link-Layer Switch` — это статья про устройство, которое пересылает кадры внутри локального сегмента сети, опираясь на link-layer адреса и соответствие адресов физическим портам.

## Основная идея или механизм

`Link-Layer Switch` не выбирает межсетевой маршрут, а решает, через какой локальный порт нужно передать кадр внутри LAN. Обычно для этого switch использует таблицу соответствия адресов и портов, формируемую по наблюдаемому трафику.

## Границы темы

- Входит: switching на уровне link layer, локальная пересылка кадров и различие с router.
- Не входит: полный разбор spanning tree, VLAN, multilayer switching и vendor-specific features.

## Связи с другими заметками

Родительская тема:

`[[Packet Switches]]`

Связанные заметки:

- `[[Data Link Layer]]`
- `[[Link Layer Protocols]]`
- `[[Packet Switches]]`
- `[[Router]]`

## Примеры, случаи или следствия

Link-layer switch удобно понимать как устройство внутренней коммутации в локальной сети: оно соединяет хосты и локальные сегменты без необходимости маршрутизации между разными IP-сетями. Именно поэтому switch и router полезно сравнивать рядом, а не по отдельности.

## Что стоит раскрыть дальше

- [ ] Добавить связь между `Link-Layer Switch` и bridge
- [ ] Уточнить границу между `Link-Layer Switch` и multilayer switch
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
