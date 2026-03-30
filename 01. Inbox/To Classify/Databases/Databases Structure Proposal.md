---
aliases:
  - Databases Structure Proposal
  - Структура ветки Databases
note_type: article
area: computer-science
domain: databases
section:
parent: "[[Computer Science]]"
status: draft
related:
  - "[[Databases]]"
  - "[[Database Transactions]]"
  - "[[ACID]]"
  - "[[Transaction Isolation]]"
  - "[[Transaction Isolation Levels]]"
  - "[[Redis]]"
  - "[[Redis Sorted Set]]"
tags: []
---

# Databases Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию domain-root ветки `Databases` внутри `Computer Science` по правилам `Principia Rerum`.

## Словарная рамка для рабочей ветки

- `domain: databases`
- `section: transactions`
- `section: redis`

## Рекомендуемая иерархия

```text
Computer Science
└── Databases
    ├── Database Transactions
    │   └── ACID
    │       ├── Transaction Atomicity
    │       ├── Transaction Consistency
    │       ├── Transaction Isolation
    │       │   └── Transaction Isolation Levels
    │       │       ├── Isolation Anomalies
    │       │       ├── Read Uncommitted
    │       │       ├── Read Committed
    │       │       ├── Repeatable Read
    │       │       ├── Serializable
    │       │       └── Snapshot Isolation
    │       └── Transaction Durability
    └── Redis
        └── Redis Sorted Set
```

## Как читать эту иерархию

- `Databases` — это domain-root overview для всей database-ветки внутри `Computer Science`.
- Внутри него сейчас оправданы две разные линии роста, а не один плоский список заметок:
  - `Database Transactions` собирает темы про корректность изменений, ACID и транзакционную семантику;
  - `Redis` собирает product-specific темы про Redis как in-memory data structure store.
- `Database Transactions` в этой модели работает как первый устойчивый sub-overview внутри domain `databases`, хотя формально сам остаётся обычной канонической overview-заметкой со своим `section: transactions`.
- Ветка `Database Transactions -> ACID` здесь принципиальна: `ACID` выступает не просто соседней заметкой, а обзорным узлом второго уровня для четырёх свойств транзакционной модели.
- `Transaction Atomicity`, `Transaction Consistency`, `Transaction Isolation` и `Transaction Durability` не являются peer-ветками рядом с `Database Transactions`: это дочерние статьи внутри `ACID`.
- `Transaction Isolation Levels` не подчиняется напрямую `Database Transactions` и не стоит на одном уровне с `ACID`: он вложен в `Transaction Isolation` как более детальная обзорная подветка свойства isolation.
- `Transaction Isolation Levels` уже выступает локальным обзорным узлом следующего уровня, потому что внутри него естественно группируются конкретные уровни изоляции и `Isolation Anomalies`.
- `Redis Sorted Set` — это обычная article-note на нижнем уровне дерева: конкретный примитив внутри product-specific ветки `Redis`, а не отдельный обзорный кластер.

## Почему структура именно такая

- `Databases` оправдан как domain-root overview, потому что тема уже не сводится к одному механизму и в ней видны разные осмысленные линии роста.
- `Databases` не стоит описывать как просто список database concepts: по правилам `Principia Rerum` здесь важнее показать несколько устойчивых смысловых подветок, чем перечислить все возможные термины на одном уровне.
- `Database Transactions` лучше держать первым устойчивым sub-overview, потому что вокруг него уже собран реальный кластер заметок о корректности, фиксации изменений, ACID и уровнях изоляции.
- `ACID` логичнее подчинять `Database Transactions`, а не держать peer-узлом рядом с `Redis` или другими будущими database-ветками, потому что по смыслу это обзорный контракт именно транзакционной модели.
- Внутри `ACID` уже оправдана собственная дочерняя структура: `Atomicity`, `Consistency`, `Isolation` и `Durability` — это разные аспекты одного обзорного узла, а не случайный набор связанных статей.
- `Transaction Isolation` лучше сохранять как промежуточный обзорный узел между `ACID` и `Transaction Isolation Levels`, потому что он описывает само свойство isolation как часть ACID, тогда как `Transaction Isolation Levels` описывает уже шкалу допустимых компромиссов.
- `Transaction Isolation Levels` уже оправдан как обзорный узел внутри ветки `Transaction Isolation`, потому что он собирает не один термин, а набор связанных notes про аномалии и конкретные уровни изоляции.
- `Redis` оправдан как отдельный section-level overview внутри `databases`, потому что это уже не просто один термин, а product-specific кластер тем про data structures, TTL, persistence и operational behavior.
- `Redis Sorted Set` должен оставаться обычной `article`, а не отдельным overview-уровнем, потому что это конкретный примитив внутри Redis.

## Что не стоит делать прямо сейчас

- Не стоит преждевременно заводить широкие sibling-ветки вроде `Storage Engines`, `Query Processing`, `Index Structures` или `Data Modeling`, пока под них нет устойчивого корпуса самостоятельных notes.
- Не стоит смешивать `Redis`-ветку с `Distributed Cache` как будто это одна и та же иерархия: связь между ними поперечная, а не родительская.
- Не стоит поднимать `ACID` обратно на один уровень с `Databases`, если ветка `Database Transactions -> ACID` уже работает как естественный узел сборки.
- Не стоит перепрыгивать через `Transaction Isolation` и описывать дерево как `Database Transactions -> Transaction Isolation Levels`, если в корпусе уже оформлен промежуточный обзорный узел свойства isolation.
- Не стоит создавать специальные templates под database notes: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── ACID.md
├── D/
│   ├── Databases.md
│   └── Database Transactions.md
├── R/
│   ├── Redis.md
│   └── Redis Sorted Set.md
└── T/
    └── Transaction Isolation Levels.md
```

## Что уже создано в Inbox

- `[[Databases]]`
- `[[Redis]]`
- `[[Redis Sorted Set]]`

## Что уже существует в Corpus Mundi или соседних ветках

- `[[Database Transactions]]`
- `[[ACID]]`
- `[[Transaction Isolation]]`
- `[[Transaction Isolation Levels]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `transactions` и `redis` нужны другие section-level кластеры
- [ ] Проверить, нужен ли позже отдельный overview про database internals
- [ ] Проверить `related`
