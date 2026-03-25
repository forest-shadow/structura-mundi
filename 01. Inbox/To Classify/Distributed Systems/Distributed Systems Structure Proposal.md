---
aliases:
  - Distributed Systems Structure Proposal
note_type: article
area: computer-science
domain: distributed-systems
section:
parent: "[[Computer Science]]"
status: draft
related:
  - "[[Distributed Systems]]"
  - "[[Distributed Systems Problems]]"
  - "[[Caching]]"
tags: []
---

# Distributed Systems Structure Proposal

## Краткое определение

Предлагаемое устройство domain-root ветки `Distributed Systems` внутри `Computer Science`.

## Рекомендуемая иерархия

```text
Computer Science
└── Distributed Systems
    ├── Distributed Systems Problems
    │   ├── Partial Failure
    │   ├── Time and Ordering
    │   ├── Consistency Under Replication
    │   └── Coordination and Consensus
    ├── Caching
    │   ├── Types of Caches
    │   │   ├── Application Cache
    │   │   ├── Database Cache
    │   │   ├── Browser and HTTP Cache
    │   │   ├── CDN and Edge Cache
    │   │   └── Distributed Cache
    │   ├── Caching Strategies
    │   │   ├── Cache-Aside Strategy
    │   │   ├── Read-Through and Refresh-Ahead Caching
    │   │   ├── Write-Through and Write-Back Caching
    │   │   ├── Write-Around Caching
    │   │   ├── Stale-While-Revalidate
    │   │   └── Negative Caching
    │   ├── Cache Invalidation
    │   │   ├── TTL-Based Invalidation
    │   │   ├── Event-Driven Invalidation
    │   │   ├── Version-Based Invalidation
    │   │   └── Tag-Based Invalidation
    │   ├── Cache Policies
    │   │   ├── Eviction Policies
    │   │   ├── Expiration Policies
    │   │   └── Admission Policies
    │   └── Cache Stampede
    ├── Event-Driven Architecture
    ├── Dual Write
    └── Telemetry
```

## Почему структура именно такая

- `Distributed Systems` оправдан как domain-root overview, потому что здесь уже есть несколько самостоятельных подветок: фундаментальные ограничения, performance-oriented caching, прикладные архитектурные паттерны и operational observability.
- `Distributed Systems Problems` остается фундаментальным sub-overview, потому что без него прикладные решения вроде caching и event-driven architecture теряют объяснительный контекст.
- `Caching` уже оправдан как отдельный `sub-overview`, потому что в распределенных системах кэш перестает быть локальной микрооптимизацией и становится отдельным слоем trade-offs между latency, load и consistency.
- `Event-Driven Architecture` и `Dual Write` остаются отдельными article-notes, потому что они уже устойчивы как прикладные архитектурные паттерны, но пока не требуют более глубокой вложенности.
- `Telemetry` стоит рядом как operational branch, потому что наблюдаемость в распределенных системах не внешняя тема, а необходимый слой эксплуатации.

## Что не стоит делать прямо сейчас

- Не стоит преждевременно вводить промежуточный overview только для performance topics сверх уже созданного `Caching`.
- Не стоит смешивать distributed-systems fundamentals с generic system-design notes без явной причины.
- Не стоит создавать специальные templates под distributed-systems branches.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный sub-overview про consistency models
- [ ] Решить, когда рядом нужны `Service Discovery` и `Load Balancing`
- [ ] Проверить `related`
