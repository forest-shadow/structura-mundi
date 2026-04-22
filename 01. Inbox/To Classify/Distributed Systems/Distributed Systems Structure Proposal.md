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
  - "[[Performance Optimization]]"
  - "[[Caching]]"
  - "[[Event-Driven Architecture]]"
  - "[[Messaging and Coordination Models]]"
  - "[[Kafka]]"
  - "[[Service Reliability]]"
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
    │   ├── Coordination and Consensus
    │   └── Dual Write
    │       ├── Polling Publisher
    │       ├── Change Data Capture
    │       └── Distributed Transaction
    ├── Performance Optimization
    │   ├── Caching
    │   │   ├── Types of Caches
    │   │   ├── Caching Strategies
    │   │   ├── Cache Invalidation
    │   │   ├── Cache Policies
    │   │   └── Cache Stampede
    │   ├── Load Balancing
    │   ├── Backpressure and Flow Control
    │   ├── Rate Limiting and Load Shedding
    │   ├── Batching and Request Coalescing
    │   ├── Partitioning and Sharding
    │   ├── Read Scaling and Replication
    │   ├── Data Locality and Placement
    │   ├── Async Processing and Queues
    │   ├── Connection Management
    │   ├── Serialization and Compression
    │   ├── Hotspot Mitigation
    │   ├── Capacity Planning and Autoscaling
    │   └── Distributed Systems Performance Modeling
    ├── Event-Driven Architecture
    │   ├── Event Collaboration Patterns
    │   │   ├── Event Notification
    │   │   ├── Event-Carried State Transfer
    │   │   └── Competing Consumers
    │   └── Idempotent Consumer
    ├── Messaging and Coordination Models
    │   ├── Brokered Messaging Model
    │   ├── Publish-Subscribe
    │   ├── Producer-Consumer Model
    │   └── Gossip Model
    ├── Kafka
    │   ├── Kafka Topic
    │   ├── Kafka Partition
    │   ├── Kafka Consumer Group
    │   └── Kafka Offset
    └── Service Reliability
        ├── Service Level Management
        ├── Telemetry
        ├── Observability
        │   └── Monitoring
        │       ├── Dashboard
        │       ├── Synthetic Monitoring
        │       └── White-box and Black-box Monitoring
        └── Alerting and Monitoring Practices
```

Переиспользуемая соседняя заметка:

- `Transactional Outbox`

## Почему структура именно такая

- `Distributed Systems` оправдан как domain-root overview, потому что здесь уже есть несколько самостоятельных подветок: фундаментальные ограничения, performance optimization, event-driven patterns и service reliability.
- `Distributed Systems Problems` остается фундаментальным sub-overview, потому что без него прикладные решения вроде caching и event-driven architecture теряют объяснительный контекст.
- `Dual Write` лучше отражать внутри `Distributed Systems Problems`, а не как отдельного top-level sibling: по смыслу это problem-centered ветка про рассогласование побочных эффектов, даже если она тесно пересекается с EDA.
- `Performance Optimization` оправдан как отдельный `sub-overview`, потому что performance-темы шире `Caching` и включают load balancing, backpressure, rate limiting, partitioning, read scaling, batching и capacity planning.
- `Event-Driven Architecture` уже стоит показывать не просто как одиночную article-note, а как полноценную архитектурную подветку с собственными дочерними темами.
- `Messaging and Coordination Models` стоит держать рядом с `Event-Driven Architecture`, а не внутри нее: pub-sub, brokered messaging, producer-consumer и gossip шире любой одной архитектурной школы и могут использоваться вне EDA.
- `Kafka` стоит держать отдельной product-specific веткой рядом с абстрактными messaging notes, а не подчинять `Messaging and Coordination Models`: эта технология образует собственный кластер заметок про topics, partitions, offsets и consumer coordination.
- `Service Reliability` стоит рядом как operational branch, потому что наблюдаемость, service levels и alerting в распределенных системах естественно собираются именно вокруг надежности сервиса.
- `Observability` лучше выделять в отдельный sub-overview внутри `Service Reliability`, а не склеивать с monitoring в одном каноническом узле: observability задает более широкую инженерную рамку, а monitoring выступает ее прикладной operational-подветкой.

## Что не стоит делать прямо сейчас

- Не стоит вытаскивать `Dual Write` обратно на уровень sibling рядом с `Distributed Systems Problems`, если её фактическая и смысловая позиция уже определена как дочерняя problem-ветка.
- Не стоит смешивать distributed-systems fundamentals с generic software-architecture notes без явной причины.
- Не стоит держать `Publish-Subscribe` только внутри `Event-Driven Architecture`, если заметка претендует на более общий distributed interaction смысл.
- Не стоит подчинять `Kafka` заметке `Brokered Messaging Model` или всей ветке `Messaging and Coordination Models`, если речь идет о product-specific корпусе, а не об абстрактном паттерне.
- Не стоит создавать специальные templates под distributed-systems branches.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный sub-overview про consistency models
- [ ] Решить, когда рядом нужен отдельный `Service Discovery`
- [ ] Подтвердить `section: messaging-and-coordination-models`
- [ ] Подтвердить `section: kafka`
- [ ] Проверить `related`
