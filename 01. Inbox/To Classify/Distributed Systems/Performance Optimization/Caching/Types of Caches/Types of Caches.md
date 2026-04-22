---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Caching]]"
status: seed
related:
  - "[[Caching]]"
  - "[[Application Cache]]"
  - "[[Distributed Cache]]"
  - "[[CDN and Edge Cache]]"
tags: []
---

# Types of Caches

## Краткое определение области

`Types of Caches` — это обзорная заметка про основные виды кэшей, различающиеся по месту расположения, роли в системе и характеру взаимодействия с source of truth.

## Что входит в эту тему

- `[[Application Cache]]`
- `[[Database Cache]]`
- `[[Browser and HTTP Cache]]`
- `[[CDN and Edge Cache]]`
- `[[Distributed Cache]]`

## Как устроена ветка

- `Application Cache` описывает локальный кэш внутри приложения или сервиса.
- `Database Cache` фиксирует кэширование на уровне запросов, результатов или access layer вокруг базы данных.
- `Browser and HTTP Cache` собирает клиентские и protocol-level кэши.
- `CDN and Edge Cache` показывает кэширование на сетевой границе.
- `Distributed Cache` описывает shared cache как инфраструктурный компонент распределённой системы.

## Рекомендуемый маршрут чтения

1. Начать с `[[Application Cache]]`.
2. Затем перейти к `[[Distributed Cache]]`.
3. После этого читать `[[Database Cache]]`.
4. Завершить `[[Browser and HTTP Cache]]` и `[[CDN and Edge Cache]]` как внешними и edge-oriented вариантами.

## Соседние overview-ветки

- `[[Caching]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Near Cache`
- [ ] Решить, когда нужен отдельный article про `DNS Cache`
- [ ] Проверить `related`
