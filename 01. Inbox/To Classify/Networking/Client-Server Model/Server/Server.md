---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-models
parent: "[[Client-Server Model]]"
status: seed
related:
  - "[[Client-Server Model]]"
  - "[[Client]]"
  - "[[Server Application]]"
  - "[[Server Process]]"
  - "[[Server Host]]"
  - "[[Service Endpoint]]"
tags: []
---

# Server

## Краткое определение области

`Server` - это обзорная заметка о многослойном термине, который в первичном смысле обозначает роль в сетевом взаимодействии, а в практической инженерной речи также может обозначать программу, процесс, хост или сетевую точку входа.

## Что входит в эту тему

- `[[Server Application]]`
- `[[Server Process]]`
- `[[Server Host]]`
- `[[Service Endpoint]]`

## Как устроена ветка

- На первичном уровне `server` означает сторону, принимающую входящие обращения и предоставляющую сервис.
- На следующем уровне `server` может обозначать программную реализацию этой роли, то есть `[[Server Application]]`.
- В operational-разговоре термин часто сужается до `[[Server Process]]`, то есть процесса или группы процессов, которые слушают сеть и обрабатывают запросы.
- Вторичное и менее строгое употребление - `[[Server Host]]`, когда словом server называют машину, VM или node, где размещен сервис.
- Еще одно частое смешение связано с `[[Service Endpoint]]`, который является не самим сервером, а сетевой точкой входа сервиса.

## Рекомендуемый маршрут чтения

1. Зафиксировать `Server` как роль и service-providing component.
2. Затем перейти к `[[Server Application]]`.
3. После этого читать `[[Server Process]]` как operational-слой.
4. В конце сопоставить с `[[Server Host]]` и `[[Service Endpoint]]`, чтобы снять терминологическую путаницу.

## Соседние overview-ветки

- Родительская рамка: `[[Client-Server Model]]`
- Прикладная языковая реализация: `[[Go Servers]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Load Balancer` и `Reverse Proxy`
- [ ] Проверить границу между `Server Application` и `Server Process`
- [ ] Проверить `related`
