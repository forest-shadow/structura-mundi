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
  - "[[Database Partitioning]]"
  - "[[Horizontal Partitioning]]"
  - "[[Partitioning Strategy Selection]]"
  - "[[Sharding]]"
  - "[[Database Connection Pooling]]"
  - "[[Database Transactions]]"
  - "[[ACID]]"
  - "[[Transaction Isolation]]"
  - "[[Transaction Isolation Levels]]"
  - "[[Redis]]"
  - "[[Redis Sorted Set]]"
  - "[[PostgreSQL]]"
  - "[[PostgreSQL Transaction Isolation]]"
tags: []
---

# Databases Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию domain-root ветки `Databases` внутри `Computer Science` по правилам `Principia Rerum`.

## Словарная рамка для рабочей ветки

- `domain: databases`
- `section: database-partitioning`
- `section: transactions`
- `section: redis`
- `section: database-connections`
- `section: postgresql`

## Рекомендуемая иерархия

```text
Computer Science
└── Databases
    ├── Database Partitioning
    │   ├── Horizontal Partitioning
    │   │   ├── Range Partitioning
    │   │   ├── Hash Partitioning
    │   │   ├── List Partitioning
    │   │   └── Composite Partitioning
    │   ├── Vertical Partitioning
    │   ├── Partition Key
    │   ├── Partition Pruning
    │   ├── Partitioning Trade-offs
    │   ├── Partitioning Strategy Selection
    │   └── Sharding
    ├── Database Connection Pooling
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
    ├── Redis
    │   └── Redis Sorted Set
    └── PostgreSQL
        ├── PostgreSQL Architecture
        └── PostgreSQL Transaction Isolation
```

## Как читать эту иерархию

- `Databases` — это domain-root overview для всей database-ветки внутри `Computer Science`.
- Внутри него сейчас оправданы несколько разные линии роста, а не один плоский список заметок:
  - `Database Partitioning` собирает темы про физическое разбиение больших таблиц, выбор partition key, pruning, эксплуатационные trade-offs и переход к distributed layout через `Sharding`;
  - `Database Transactions` собирает темы про корректность изменений, ACID и транзакционную семантику;
  - `Database Connection Pooling` собирает database-specific perspective на работу пула соединений, connection budget, saturation и operational tuning;
  - `Redis` собирает product-specific темы про Redis как in-memory data structure store;
  - `PostgreSQL` собирает product-specific темы про PostgreSQL как реляционную СУБД общего назначения.
- `Database Partitioning` в этой модели работает как отдельный section-level overview внутри domain `databases`: вокруг темы уже естественно группируются виды partitioning, выбор стратегии, partition pruning и distributed variant в виде `Sharding`.
- `Database Connection Pooling` не является дочерней статьей `Connection Pooling`: общая статья про pooling-pattern живет в другой доменной оптике и связывается только через `related`.
- `Database Transactions` в этой модели работает как первый устойчивый sub-overview внутри domain `databases`, хотя формально сам остаётся обычной канонической overview-заметкой со своим `section: transactions`.
- Ветка `Database Transactions -> ACID` здесь принципиальна: `ACID` выступает не просто соседней заметкой, а обзорным узлом второго уровня для четырёх свойств транзакционной модели.
- `Transaction Atomicity`, `Transaction Consistency`, `Transaction Isolation` и `Transaction Durability` не являются peer-ветками рядом с `Database Transactions`: это дочерние статьи внутри `ACID`.
- `Transaction Isolation Levels` не подчиняется напрямую `Database Transactions` и не стоит на одном уровне с `ACID`: он вложен в `Transaction Isolation` как более детальная обзорная подветка свойства isolation.
- `Transaction Isolation Levels` уже выступает локальным обзорным узлом следующего уровня, потому что внутри него естественно группируются конкретные уровни изоляции и `Isolation Anomalies`.
- `Redis Sorted Set` — это обычная article-note на нижнем уровне дерева: конкретный примитив внутри product-specific ветки `Redis`, а не отдельный обзорный кластер.
- `PostgreSQL Architecture` и `PostgreSQL Transaction Isolation` — это обычные product-specific article-заметки внутри `PostgreSQL`, а не отдельные overview-ветки. Пока их разумнее держать плоскими sibling-узлами под product overview.
- `Sharding` пока лучше оставлять дочерней article-note внутри `Database Partitioning`, а не выносить в отдельный overview: сейчас важнее зафиксировать его как distributed extension горизонтального partitioning, чем преждевременно строить вокруг него новую большую ветку.

## Почему структура именно такая

- `Databases` оправдан как domain-root overview, потому что тема уже не сводится к одному механизму и в ней видны разные осмысленные линии роста.
- `Databases` не стоит описывать как просто список database concepts: по правилам `Principia Rerum` здесь важнее показать несколько устойчивых смысловых подветок, чем перечислить все возможные термины на одном уровне.
- `Database Partitioning` лучше держать отдельным overview-узлом, потому что тема уже распадается на несколько устойчивых смысловых вопросов: как именно делятся данные, по какому ключу, когда это действительно оправдано, какие издержки это несет и когда partitioning переходит в sharding.
- `Database Transactions` лучше держать первым устойчивым sub-overview, потому что вокруг него уже собран реальный кластер заметок о корректности, фиксации изменений, ACID и уровнях изоляции.
- `Database Connection Pooling` лучше держать отдельной article-note прямо под `Databases`, потому что это уже database-specific operational topic, но пока еще не самостоятельный обзорный кластер.
- `Horizontal Partitioning` оправдан как вложенный overview внутри `Database Partitioning`, потому что range, hash, list и composite — это не случайный перечень терминов, а естественное семейство row-based strategies.
- `Vertical Partitioning` пока достаточно одной article-note, потому что рядом еще нет устойчивого корпуса дочерних заметок про column families, hot/cold split или storage-tier-specific decomposition.
- `Partition Key`, `Partition Pruning`, `Partitioning Trade-offs` и `Partitioning Strategy Selection` разумнее держать отдельными статьями рядом с типами partitioning, потому что они отвечают на разные инженерные вопросы: как маршрутизировать данные, как получать выигрыш, какой ценой и в каких workload-сценариях strategy вообще стоит применять.
- `ACID` логичнее подчинять `Database Transactions`, а не держать peer-узлом рядом с `Redis`, `PostgreSQL` или другими будущими database-ветками, потому что по смыслу это обзорный контракт именно транзакционной модели.
- Внутри `ACID` уже оправдана собственная дочерняя структура: `Atomicity`, `Consistency`, `Isolation` и `Durability` — это разные аспекты одного обзорного узла, а не случайный набор связанных статей.
- `Transaction Isolation` лучше сохранять как промежуточный обзорный узел между `ACID` и `Transaction Isolation Levels`, потому что он описывает само свойство isolation как часть ACID, тогда как `Transaction Isolation Levels` описывает уже шкалу допустимых компромиссов.
- `Transaction Isolation Levels` уже оправдан как обзорный узел внутри ветки `Transaction Isolation`, потому что он собирает не один термин, а набор связанных notes про аномалии и конкретные уровни изоляции.
- `Redis` оправдан как отдельный section-level overview внутри `databases`, потому что это уже не просто один термин, а product-specific кластер тем про data structures, TTL, persistence и operational behavior.
- `PostgreSQL` тоже оправдан как отдельный section-level overview внутри `databases`, потому что это не один термин, а устойчивый product-specific кластер вокруг архитектуры сервера, транзакционного поведения, MVCC и эксплуатационных механизмов.
- `PostgreSQL Transaction Isolation` не стоит делать дублем общей ветки `Transaction Isolation Levels`: это должна быть PostgreSQL-specific статья о том, как общие уровни и аномалии реально интерпретируются в PostgreSQL.

## Что не стоит делать прямо сейчас

- Не стоит преждевременно заводить широкие sibling-ветки вроде `Storage Engines`, `Query Processing`, `Index Structures` или `Data Modeling`, пока под них нет устойчивого корпуса самостоятельных notes.
- Не стоит преждевременно заводить отдельные overview-узлы `Partition Types`, `Partitioning Use Cases` или `Partitioning Operations`: текущая ветка `Database Partitioning` уже покрывает эти вопросы без лишнего уровня вложенности.
- Не стоит смешивать `Redis`-ветку с `Distributed Cache` как будто это одна и та же иерархия: связь между ними поперечная, а не родительская.
- Не стоит подчинять `Database Connection Pooling` общей статье `Connection Pooling`, потому что это создает ложную иерархию между разными domain perspectives.
- Не стоит делать `Sharding` peer-узлом рядом с `Databases`, если пока речь идет именно о distributed form database partitioning, а не о самостоятельной distributed-systems ветке с собственным большим корпусом.
- Не стоит сразу плодить product-specific notes вроде `PostgreSQL Range Partitioning` или `PostgreSQL Partition Pruning`, пока общая database-ветка еще не заполнена базовыми каноническими заметками.
- Не стоит поднимать `ACID` обратно на один уровень с `Databases`, если ветка `Database Transactions -> ACID` уже работает как естественный узел сборки.
- Не стоит перепрыгивать через `Transaction Isolation` и описывать дерево как `Database Transactions -> Transaction Isolation Levels`, если в корпусе уже оформлен промежуточный обзорный узел свойства isolation.
- Не стоит делать отдельные заметки `PostgreSQL Read Committed`, `PostgreSQL Repeatable Read` и `PostgreSQL Serializable`, пока PostgreSQL-specific семантика этих уровней еще помещается в одну цельную article-note.
- Не стоит создавать специальные templates под database notes или под `PostgreSQL`: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── ACID.md
├── C/
│   └── Composite Partitioning.md
├── D/
│   ├── Databases.md
│   ├── Database Partitioning.md
│   ├── Database Connection Pooling.md
│   └── Database Transactions.md
├── H/
│   ├── Horizontal Partitioning.md
│   └── Hash Partitioning.md
├── L/
│   └── List Partitioning.md
├── P/
│   ├── Partition Key.md
│   ├── Partition Pruning.md
│   ├── Partitioning Strategy Selection.md
│   ├── Partitioning Trade-offs.md
│   ├── PostgreSQL.md
│   ├── PostgreSQL Architecture.md
│   └── PostgreSQL Transaction Isolation.md
├── R/
│   ├── Range Partitioning.md
│   ├── Redis.md
│   └── Redis Sorted Set.md
├── S/
│   └── Sharding.md
├── V/
│   └── Vertical Partitioning.md
└── T/
    └── Transaction Isolation Levels.md
```

## Что уже создано в Inbox

- `[[Database Partitioning]]`
- `[[Horizontal Partitioning]]`
- `[[Vertical Partitioning]]`
- `[[Partition Key]]`
- `[[Partition Pruning]]`
- `[[Partitioning Trade-offs]]`
- `[[Partitioning Strategy Selection]]`
- `[[Sharding]]`
- `[[Range Partitioning]]`
- `[[Hash Partitioning]]`
- `[[List Partitioning]]`
- `[[Composite Partitioning]]`
- `[[Databases]]`
- `[[Redis]]`
- `[[Redis Sorted Set]]`
- `[[Database Connection Pooling]]`
- `[[PostgreSQL]]`
- `[[PostgreSQL Architecture]]`
- `[[PostgreSQL Transaction Isolation]]`

## Что уже существует в Corpus Mundi или соседних ветках

- `[[Database Transactions]]`
- `[[ACID]]`
- `[[Transaction Isolation]]`
- `[[Transaction Isolation Levels]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `transactions`, `database-partitioning`, `redis` и `postgresql` нужны другие section-level кластеры
- [ ] Проверить, когда рядом с общей веткой нужен product-specific overview вроде `PostgreSQL Partitioning`
- [ ] Проверить, нужен ли позднее отдельный overview `Database Connections`, если рядом появятся `DB Proxy`, `PgBouncer` и `Connection Budget`
- [ ] Проверить, нужен ли позже отдельный overview про database internals
- [ ] Проверить, когда PostgreSQL-ветка доросла до отдельных notes про MVCC, WAL и vacuum
- [ ] Проверить `related`
