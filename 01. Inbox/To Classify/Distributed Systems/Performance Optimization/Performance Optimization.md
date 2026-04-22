---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Distributed Systems]]"
status: seed
related:
  - "[[Distributed Systems]]"
  - "[[Caching]]"
  - "[[Load Balancing]]"
  - "[[Backpressure and Flow Control]]"
  - "[[Rate Limiting and Load Shedding]]"
  - "[[Batching and Request Coalescing]]"
  - "[[Partitioning and Sharding]]"
  - "[[Read Scaling and Replication]]"
  - "[[Data Locality and Placement]]"
  - "[[Async Processing and Queues]]"
  - "[[Connection Management]]"
  - "[[Serialization and Compression]]"
  - "[[Hotspot Mitigation]]"
  - "[[Capacity Planning and Autoscaling]]"
  - "[[Distributed Systems Performance Modeling]]"
tags: []
---

# Performance Optimization

## Краткое определение области

`Performance Optimization` — это обзорная ветка про способы снижать latency, повышать throughput, сглаживать пики нагрузки и управлять saturation в распределенных системах.

## Что входит в эту тему

- `[[Caching]]`
- `[[Load Balancing]]`
- `[[Backpressure and Flow Control]]`
- `[[Rate Limiting and Load Shedding]]`
- `[[Batching and Request Coalescing]]`
- `[[Partitioning and Sharding]]`
- `[[Read Scaling and Replication]]`
- `[[Data Locality and Placement]]`
- `[[Async Processing and Queues]]`
- `[[Connection Management]]`
- `[[Serialization and Compression]]`
- `[[Hotspot Mitigation]]`
- `[[Capacity Planning and Autoscaling]]`
- `[[Distributed Systems Performance Modeling]]`

## Как устроена ветка

- `Caching` уменьшает количество дорогих обращений к source of truth и добавляет trade-offs freshness, invalidation и consistency.
- `Load Balancing`, `Partitioning and Sharding` и `Read Scaling and Replication` распределяют работу между узлами, репликами и шардами.
- `Backpressure and Flow Control`, `Rate Limiting and Load Shedding` и `Capacity Planning and Autoscaling` защищают систему от перегруза.
- `Batching and Request Coalescing`, `Async Processing and Queues`, `Connection Management`, `Serialization and Compression` уменьшают стоимость обработки и передачи единицы работы.
- `Data Locality and Placement` и `Hotspot Mitigation` работают с тем, где находится нагрузка и почему она концентрируется.
- `Distributed Systems Performance Modeling` связывает практические оптимизации с моделями latency, throughput, concurrency и saturation.

## Рекомендуемый маршрут чтения

1. Начать с `[[Distributed Systems Performance Modeling]]`, чтобы задать язык latency, throughput и saturation.
2. Затем читать `[[Caching]]`, `[[Load Balancing]]` и `[[Partitioning and Sharding]]` как базовые способы разгрузки системы.
3. После этого перейти к `[[Backpressure and Flow Control]]` и `[[Rate Limiting and Load Shedding]]`.
4. Завершить прикладными механизмами: `[[Batching and Request Coalescing]]`, `[[Connection Management]]`, `[[Serialization and Compression]]`, `[[Hotspot Mitigation]]`.

## Соседние overview-ветки

- `[[Distributed Systems Problems]]`
- `[[Service Reliability]]`
- `[[Messaging and Coordination Models]]`
- `[[Performance Modeling]]`

