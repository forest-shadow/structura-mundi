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
  - "[[Network Topology]]"
  - "[[Network Performance]]"
  - "[[Network Protocols]]"
  - "[[Packet Switches]]"
  - "[[Internet]]"
  - "[[OSI Model]]"
tags: []
---

# Networking

## Краткое определение области

`Networking` — это доменная обзорная ветка внутри `computer-science`, которая собирает заметки о соединении сетевых узлов, передаче данных, сетевых протоколах, переключении пакетов, моделях сетевого стека и операционном устройстве Internet.

## Что входит в эту тему

- `[[Network Topology]]`
- `[[Network Performance]]`
- `[[Network Protocols]]`
- `[[Packet Switches]]`
- `[[Internet]]`
- `[[OSI Model]]`

## Как устроена ветка

- `Network Topology` описывает форму и связность сети как структуры.
- `Network Performance` собирает метрики пропускной способности, задержек, джиттера и потерь.
- `Network Protocols` держит рамку для семейств протоколов и их роли в сетевом стеке.
- `Packet Switches` собирает устройства пересылки данных вроде `Router` и `Link-Layer Switch`, не смешивая их ни с протоколами, ни с topology patterns.
- `Internet` удерживает operational-взгляд на современный TCP/IP мир.
- `OSI Model` остаётся соседней концептуальной моделью сетевых функций.

## Рекомендуемый маршрут чтения

1. Начать с `[[Networking]]`.
2. Затем выбрать ракурс: структура через `[[Network Topology]]`, качество доставки через `[[Network Performance]]` или правила взаимодействия через `[[Network Protocols]]`.
3. После этого перейти к `[[Packet Switches]]`, если нужен язык для описания устройств пересылки.
4. Затем читать `[[Internet]]` и сопоставлять operational-картину с `[[OSI Model]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужен `Network Security`
- [ ] Решить, когда рядом нужен `Network Congestion`
- [ ] Проверить границу между `Packet Switches` и `Network Protocols`
- [ ] Проверить `related`
