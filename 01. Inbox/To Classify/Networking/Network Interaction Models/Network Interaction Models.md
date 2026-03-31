---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-models
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[Client-Server Model]]"
  - "[[Peer-to-Peer Model]]"
  - "[[Request-Reply Model]]"
  - "[[Broadcast and Multicast Model]]"
tags: []
---

# Network Interaction Models

## Краткое определение области

`Network Interaction Models` - это обзорная заметка о базовых формах сетевого взаимодействия между узлами: кто инициирует обмен, как распределяются роли и сколько участников вовлечено в доставку сообщения или ответа.

## Что входит в эту тему

- `[[Client-Server Model]]`
- `[[Peer-to-Peer Model]]`
- `[[Request-Reply Model]]`
- `[[Broadcast and Multicast Model]]`

## Как устроена ветка

- `Client-Server Model` фиксирует асимметричную модель с разделением ролей клиента и сервера.
- `Peer-to-Peer Model` фиксирует симметричное взаимодействие между узлами без постоянного центрального сервера.
- `Request-Reply Model` удерживает форму обмена запросом и ответом без привязки к единственной архитектурной реализации.
- `Broadcast and Multicast Model` описывает сетевое взаимодействие, в котором сообщение адресуется не одному узлу, а группе или всем участникам сегмента.

## Рекомендуемый маршрут чтения

1. Начать с `[[Client-Server Model]]` как с самой знакомой формы взаимодействия.
2. Затем перейти к `[[Peer-to-Peer Model]]`, чтобы увидеть модель без жесткой ролевой асимметрии.
3. После этого читать `[[Request-Reply Model]]` как более общую exchange-oriented форму.
4. Завершить `[[Broadcast and Multicast Model]]`, если нужен group-delivery взгляд.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Соседняя distributed-systems ветка: `[[Messaging and Coordination Models]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Anycast` и `Unicast`
- [ ] Проверить границу между `Request-Reply Model` и `Client-Server Model`
- [ ] Проверить `related`
