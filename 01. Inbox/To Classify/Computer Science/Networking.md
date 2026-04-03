---
aliases:
  - Computer Networking
note_type: overview
area: computer-science
domain: networking
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Network Interaction Models]]"
  - "[[Network Topology]]"
  - "[[Network Performance]]"
  - "[[Network Protocols]]"
  - "[[Proxy]]"
  - "[[Service Mesh]]"
  - "[[TLS Termination]]"
  - "[[Origin Shielding]]"
  - "[[Network Security]]"
  - "[[Packet Switches]]"
  - "[[Internet]]"
  - "[[OSI Model]]"
tags: []
---

# Networking

## Краткое определение области

`Networking` — это доменная обзорная ветка внутри `computer-science`, которая собирает заметки о соединении сетевых узлов, передаче данных, сетевых протоколах, переключении пакетов, моделях сетевого стека и операционном устройстве Internet.

## Что входит в эту тему

- `[[Network Interaction Models]]`
- `[[Network Topology]]`
- `[[Network Performance]]`
- `[[Network Protocols]]`
- `[[Proxy]]`
- `[[Service Mesh]]`
- `[[TLS Termination]]`
- `[[Origin Shielding]]`
- `[[Network Security]]`
- `[[Packet Switches]]`
- `[[Internet]]`
- `[[OSI Model]]`

## Как устроена ветка

- `Network Interaction Models` собирает базовые формы сетевого взаимодействия между узлами: client-server, peer-to-peer, request-reply, broadcast и multicast.
- `Network Topology` описывает форму и связность сети как структуры.
- `Network Performance` собирает метрики пропускной способности, задержек, джиттера и потерь.
- `Network Protocols` держит рамку для семейств протоколов и их роли в сетевом стеке.
- `Proxy`, `Service Mesh`, `TLS Termination` и `Origin Shielding` собирают intermediary-layer темы про промежуточную обработку, защиту и управление сетевым трафиком.
- `Network Security` собирает сетевые механизмы доверия, изоляции, защищенного доступа и туннелирования, не смешивая их ни с общей protocol taxonomy, ни с устройствами пересылки.
- `Packet Switches` собирает устройства пересылки данных вроде `Router` и `Link-Layer Switch`, не смешивая их ни с протоколами, ни с topology patterns.
- `Internet` удерживает operational-взгляд на современный TCP/IP мир.
- `OSI Model` остаётся соседней концептуальной моделью сетевых функций.

## Рекомендуемый маршрут чтения

1. Начать с `[[Networking]]`.
2. Затем выбрать ракурс: role/model view через `[[Network Interaction Models]]`, структура через `[[Network Topology]]`, качество доставки через `[[Network Performance]]`, правила взаимодействия через `[[Network Protocols]]` или защищенный сетевой доступ через `[[Network Security]]`.
3. После этого перейти к `[[Proxy]]`, `[[Service Mesh]]`, `[[TLS Termination]]` и `[[Origin Shielding]]`, если нужен intermediary-layer взгляд на сетевую инфраструктуру.
4. Затем перейти к `[[Packet Switches]]`, если нужен язык для описания устройств пересылки.
5. Затем читать `[[Internet]]` и сопоставлять operational-картину с `[[OSI Model]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда внутри `Network Interaction Models` нужны `Anycast` и `Unicast`
- [ ] Проверить границу между `Network Security`, `Network Protocols` и `Internet`
- [ ] Проверить границу между `Proxy`, `Service Mesh`, `TLS Termination` и `Origin Shielding`
- [ ] Решить, когда рядом нужен `Network Congestion`
- [ ] Проверить границу между `Packet Switches` и `Network Protocols`
- [ ] Проверить `related`
