---
aliases:
  - Packet-Switching Devices
note_type: overview
area: computer-science
domain: networking
section: packet-switches
parent: "[[Networking]]"
status: seed
related:
  - "[[Router]]"
  - "[[Link-Layer Switch]]"
  - "[[Routing]]"
  - "[[Network Layer]]"
  - "[[Data Link Layer]]"
tags: []
---

# Packet Switches

## Краткое определение области

`Packet Switches` — это обзорная ветка про сетевые устройства, которые принимают входящие данные, анализируют служебную информацию заголовка и пересылают трафик дальше на подходящий выходной интерфейс или next hop.

## Что входит в эту тему

- `[[Router]]`
- `[[Link-Layer Switch]]`

## Как устроена ветка

- `Router` описывает пересылку между разными сетями на основе network-layer адресации и forwarding tables.
- `Link-Layer Switch` описывает пересылку кадров внутри локального сегмента по link-layer адресам и соответствию адресов портам.
- Эти устройства полезно держать рядом, потому что оба относятся к packet-switching devices, но работают на разных уровнях и в разном масштабе.
- Ветка не должна смешивать сами устройства с protocol families или с модельными уровнями вроде `OSI Model`.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Packet Switches`.
2. Затем читать `[[Router]]`.
3. После этого перейти к `[[Link-Layer Switch]]`.
4. Затем сопоставить это с `[[Routing]]`, `[[Network Layer]]` и `[[Data Link Layer]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Близкая protocol-ветка: `[[Network Protocols]]`
- Близкая operational-ветка: `[[Internet]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Switching Fabric` и `Forwarding Table`
- [ ] Уточнить границу между `Router` и `Routing`
- [ ] Уточнить границу между `Link-Layer Switch` и bridge
- [ ] Проверить `related`
