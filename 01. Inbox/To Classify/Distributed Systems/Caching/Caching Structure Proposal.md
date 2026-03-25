---
aliases:
  - Caching Structure Proposal
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Distributed Systems]]"
status: draft
related:
  - "[[Caching]]"
  - "[[Distributed Systems]]"
  - "[[Distributed Systems Problems]]"
  - "[[Caching Strategies]]"
tags: []
---

# Caching Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Caching` внутри `Distributed Systems` как performance-oriented sub-overview.

## Рекомендуемая иерархия

```text
Distributed Systems
└── Caching
    ├── Caching Strategies
    │   ├── Cache-Aside Strategy
    │   └── Write-Through and Write-Back Caching
    ├── Cache Invalidation
    ├── Distributed Cache
    └── Cache Stampede
```

## Почему структура именно такая

- `Caching` уже оправдан как `sub-overview`, потому что тема не сводится к одному термину и внутри нее есть устойчивый набор canonical notes про стратегии, invalidation и distributed failure modes.
- `Caching Strategies` оправдан как вложенный `overview`, потому что read-path и write-path patterns образуют отдельный смысловой кластер и не должны висеть рядом с invalidation и failure modes как несвязанные peer-notes.
- `Cache Invalidation` нужен как центральная conceptual note, потому что именно там сосредоточен основной trade-off между speed и freshness.
- `Cache-Aside Strategy` и `Write-Through and Write-Back Caching` представляют разные operational patterns работы с кэшем, но на уровне ветки их лучше собирать под отдельным strategy-overview.
- `Distributed Cache` оправдан как отдельный article, потому что в распределенных системах кэш часто становится уже не локальной деталью, а shared infrastructure component.
- `Cache Stampede` нужен как типовая performance pathology, которая делает ветку ближе к реальным distributed-systems trade-offs.

## Что не стоит делать прямо сейчас

- Не стоит преждевременно выносить каждый cache backend в отдельную canonical note.
- Не стоит дробить `Write-Through` и `Write-Back` на отдельные notes, пока важнее их сравнительное рассмотрение.
- Не стоит смешивать application caching, CPU cache и browser cache в одну ветку.
- Не стоит создавать специальные templates под cache notes.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Eviction Policy`, `TTL` и `CDN`
- [ ] Проверить `related`
