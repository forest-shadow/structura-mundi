---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-protocols
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[TCP IP Model]]"
  - "[[OSI Model]]"
  - "[[Link Layer Protocols]]"
  - "[[Network Layer Protocols]]"
  - "[[Transport Layer Protocols]]"
  - "[[Application Layer Protocols]]"
  - "[[HTTP]]"
tags: []
---

# Network Protocols

## Краткое определение области

`Network Protocols` — это обзорная заметка о правилах, форматах и соглашениях, по которым сетевые узлы обмениваются данными и координируют взаимодействие.

## Что входит в эту тему

- `[[Link Layer Protocols]]`
- `[[Network Layer Protocols]]`
- `[[Transport Layer Protocols]]`
- `[[Application Layer Protocols]]`

## Как устроена ветка

- `Network Protocols` удерживает общую рамку для разговора о protocol families, а не о случайном списке отдельных имен вроде `TCP`, `HTTP` и `BGP`.
- `Link Layer Protocols`, `Network Layer Protocols`, `Transport Layer Protocols` и `Application Layer Protocols` группируют протоколы по их роли в сетевом стеке.
- `Routing Protocols` вынесены как вложенная ветка внутри `Network Layer Protocols`, потому что это устойчивый подкласс протоколов управления путями между сетями.
- `HTTP` уже вынесен как вложенная `sub-overview`-ветка внутри `Application Layer Protocols`, потому что тема быстро перестает помещаться в одну статью.
- Более узкие notes про конкретные протоколы пока не создаются, чтобы ветка не превратилась в плоский каталог до появления плотного корпуса.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Network Protocols`.
2. Затем идти снизу вверх по семействам: `[[Link Layer Protocols]]`, `[[Network Layer Protocols]]`, `[[Transport Layer Protocols]]`, `[[Application Layer Protocols]]`.
3. После этого перейти к `[[Routing Protocols]]`, если нужен отдельный взгляд на протоколы выбора маршрутов.
4. Затем внутри `[[Application Layer Protocols]]` перейти к `[[HTTP]]`, если нужен конкретный прикладной протокол.
5. Затем сопоставить ветку с `[[TCP IP Model]]` и `[[OSI Model]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Соседняя model-ветка: `[[OSI Model]]`
- Соседняя operational-ветка: `[[Internet]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `HTTP` нужны `DNS`, `SMTP` и `DHCP` как отдельные подветки
- [ ] Решить, когда нужны отдельные notes про `TCP`, `UDP`, `IP`, `ICMP` и `DHCP`
- [ ] Проверить, нужен ли отдельный узел про `Protocol Encapsulation`
- [ ] Проверить `related`
