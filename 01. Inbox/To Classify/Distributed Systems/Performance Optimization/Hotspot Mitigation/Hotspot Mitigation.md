---
aliases: []
note_type: overview
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Performance Optimization]]"
status: seed
related:
  - "[[Performance Optimization]]"
  - "[[Caching]]"
  - "[[Load Balancing]]"
  - "[[Partitioning and Sharding]]"
tags: []
---

# Hotspot Mitigation

## Краткое определение области

`Hotspot Mitigation` — это обзорная ветка про ситуации, где непропорционально большая доля нагрузки концентрируется на одном ключе, шарде, реплике, очереди, lock или downstream dependency.

## Что входит в эту тему

- hot keys
- skewed partitions
- celebrity problem
- request fan-in
- sharded counters
- cache stampede controls

## Соседние overview-ветки

- `[[Caching]]`
- `[[Load Balancing]]`
- `[[Partitioning and Sharding]]`

