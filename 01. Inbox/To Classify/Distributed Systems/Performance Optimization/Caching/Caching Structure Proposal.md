---
aliases:
  - Caching Structure Proposal
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Performance Optimization]]"
status: draft
related:
  - "[[Caching]]"
  - "[[Performance Optimization]]"
  - "[[Distributed Systems]]"
  - "[[Distributed Systems Problems]]"
  - "[[Types of Caches]]"
  - "[[Caching Strategies]]"
  - "[[Cache Policies]]"
tags: []
---

# Caching Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Caching` внутри `Performance Optimization` как performance-oriented sub-overview.

## Рекомендуемая иерархия

```text
Distributed Systems
└── Performance Optimization
    └── Caching
        ├── Types of Caches
        │   ├── Application Cache
        │   ├── Database Cache
        │   ├── Browser and HTTP Cache
        │   ├── CDN and Edge Cache
        │   └── Distributed Cache
        ├── Caching Strategies
        │   ├── Cache-Aside Strategy
        │   ├── Read-Through and Refresh-Ahead Caching
        │   ├── Write-Through and Write-Back Caching
        │   ├── Write-Around Caching
        │   ├── Stale-While-Revalidate
        │   └── Negative Caching
        ├── Cache Invalidation
        │   ├── TTL-Based Invalidation
        │   ├── Event-Driven Invalidation
        │   ├── Version-Based Invalidation
        │   └── Tag-Based Invalidation
        ├── Cache Policies
        │   ├── Eviction Policies
        │   ├── Expiration Policies
        │   └── Admission Policies
        └── Cache Stampede
```

## Почему структура именно такая

- `Caching` уже оправдан как `sub-overview`, потому что тема не сводится к одному термину и внутри нее есть устойчивые кластеры про виды кэшей, стратегии, invalidation, policies и failure modes.
- `Types of Caches` нужен как отдельный `overview`, потому что вопрос "какой именно это кэш?" отличается от вопроса "как он работает?".
- `Caching Strategies` оправдан как вложенный `overview`, потому что read-path и write-path patterns образуют отдельный смысловой кластер и не должны висеть рядом с invalidation и failure modes как несвязанные peer-notes.
- `Cache Invalidation` лучше оформлять как `overview`, потому что time-based, event-driven, version-based и tag-based invalidation представляют разные canonical mechanisms.
- `Cache Policies` нужен как отдельный `overview`, потому что admission, expiration и eviction отвечают на другой класс вопросов, чем стратегии и invalidation.
- `Distributed Cache` сохраняется как отдельный article, но логичнее расположен внутри `Types of Caches`, а не рядом с operational strategies.
- `Cache Stampede` нужен как типовая performance pathology, которая делает ветку ближе к реальным distributed-systems trade-offs.

## Что не стоит делать прямо сейчас

- Не стоит преждевременно выносить каждый cache backend в отдельную canonical note.
- Не стоит дробить все стратегии и invalidation-mechanisms до product-specific частностей.
- Не стоит дробить `Write-Through` и `Write-Back` на отдельные notes, пока важнее их сравнительное рассмотрение.
- Не стоит смешивать application caching, CPU cache и browser cache в одну ветку.
- Не стоит создавать специальные templates под cache notes.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Request Coalescing`
- [ ] Решить, когда нужен отдельный article про `Near Cache`
- [ ] Проверить `related`
