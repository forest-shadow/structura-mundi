---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-performance
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[Network Bandwidth]]"
  - "[[Network Throughput]]"
  - "[[Network Latency]]"
  - "[[Network Jitter]]"
  - "[[Network Packet Loss]]"
tags: []
---

# Network Performance

## Краткое определение области

`Network Performance` — это обзорная заметка о том, какими метриками описывают качество и емкость сетевого взаимодействия и как эти метрики ограничивают реальную передачу данных.

## Что входит в эту тему

- `[[Network Bandwidth]]`
- `[[Network Throughput]]`
- `[[Network Latency]]`
- `[[Network Jitter]]`
- `[[Network Packet Loss]]`

## Как устроена ветка

- `Network Bandwidth` фиксирует верхнюю границу пропускной способности канала или соединения как capacity concept.
- `Network Throughput` описывает реальную достигнутую скорость передачи данных и не должен смешиваться с bandwidth.
- `Network Latency`, `Network Jitter` и `Network Packet Loss` собирают соседние метрики качества доставки, которые вместе с bandwidth определяют практическое поведение сети.
- Более специальные темы вроде `Bandwidth-Delay Product`, `Quality of Service` и `Congestion Control` пока не выносятся в отдельные notes, чтобы ветка оставалась компактной.

## Рекомендуемый маршрут чтения

1. Начать с `[[Network Bandwidth]]`, чтобы зафиксировать саму идею capacity limit.
2. Затем перейти к `[[Network Throughput]]`, чтобы развести теоретический максимум и фактический результат.
3. После этого читать `[[Network Latency]]`, `[[Network Jitter]]` и `[[Network Packet Loss]]` как остальные ключевые performance-метрики.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Соседняя structural-ветка: `[[Network Topology]]`
- Соседняя operational-ветка: `[[Internet]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Bandwidth-Delay Product` и `Quality of Service`
- [ ] Проверить, нужен ли отдельный узел про `Network Congestion`
- [ ] Проверить `related`
