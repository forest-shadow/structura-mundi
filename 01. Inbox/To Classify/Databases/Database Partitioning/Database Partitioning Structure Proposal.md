---
aliases:
  - Database Partitioning Branch Structure Proposal
  - Структура ветки Database Partitioning
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Databases]]"
status: draft
related:
  - "[[Databases]]"
  - "[[Database Partitioning]]"
  - "[[Horizontal Partitioning]]"
  - "[[Vertical Partitioning]]"
  - "[[Partition Key]]"
  - "[[Partitioning Strategy Selection]]"
  - "[[Sharding]]"
tags: []
---

# Database Partitioning Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Database Partitioning` внутри `Databases` по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: databases`
- `section: database-partitioning` (предлагаемое рабочее значение)

Почему так:

- `Database Partitioning` естественно живет внутри уже существующего `domain: databases`, а не требует отдельного domain;
- рядом с темой возникает не одна статья, а реальный кластер заметок про виды разбиения, выбор partition key, pruning, trade-offs и сценарии применения;
- это уже отдельная database-specific перспектива на физическую организацию данных, а не просто частный абзац внутри `PostgreSQL` или `Sharding`.

## Рекомендуемая иерархия

```text
Databases
└── Database Partitioning
    ├── Horizontal Partitioning
    │   ├── Range Partitioning
    │   ├── Hash Partitioning
    │   ├── List Partitioning
    │   └── Composite Partitioning
    ├── Vertical Partitioning
    ├── Partition Key
    ├── Partition Pruning
    ├── Partitioning Trade-offs
    ├── Partitioning Strategy Selection
    └── Sharding
```

## Почему структура именно такая

- `Database Partitioning` лучше делать `overview`, потому что тема собирает несколько разных, но тесно связанных вопросов: как именно делятся данные, по какому признаку, какой это дает выигрыш и в каких workload-сценариях разбиение вообще оправдано.
- `Horizontal Partitioning` оправдан как вложенный `overview`, потому что `Range Partitioning`, `Hash Partitioning`, `List Partitioning` и `Composite Partitioning` образуют естественное семейство row-based strategies.
- `Vertical Partitioning` пока достаточно одной `article`, потому что рядом еще нет устойчивого корпуса отдельных notes про column-groups, hot/cold split и storage-tier decomposition.
- `Partition Key` нужен отдельной `article`, потому что выбор ключа маршрутизации определяет и равномерность распределения, и локальность запросов, и вероятность hot partitions.
- `Partition Pruning` нужен отдельной `article`, потому что это один из главных practical benefits partitioning и при этом отдельный технический механизм, связанный с planner behavior и формой запросов.
- `Partitioning Trade-offs` лучше держать отдельно, чтобы не растворять operational cost в notes про типы partitioning.
- `Partitioning Strategy Selection` отвечает на вопрос "когда и как применять partitioning", поэтому ей логично быть самостоятельной article-note.
- `Sharding` здесь лучше держать дочерней `article`, а не отдельным overview: на текущем этапе это наиболее естественно понимать как distributed extension горизонтального partitioning.

## Что не стоит делать прямо сейчас

- Не стоит сразу вводить отдельные `overview` вроде `Partition Types`, `Partitioning Operations` или `Partitioning Use Cases`: текущая ветка уже покрывает эти вопросы без лишней глубины.
- Не стоит создавать product-specific ветки `PostgreSQL Range Partitioning` или `MySQL Partition Pruning`, пока не собран общий канонический корпус по самой теме partitioning.
- Не стоит смешивать `Database Partitioning` и `Sharding` как полные синонимы: sharding лучше описывать как частный distributed deployment pattern поверх partitioning.
- Не стоит создавать специальные template-файлы под эту ветку: по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── C/
│   └── Composite Partitioning.md
├── D/
│   └── Database Partitioning.md
├── H/
│   ├── Horizontal Partitioning.md
│   └── Hash Partitioning.md
├── L/
│   └── List Partitioning.md
├── P/
│   ├── Partition Key.md
│   ├── Partition Pruning.md
│   ├── Partitioning Strategy Selection.md
│   └── Partitioning Trade-offs.md
├── R/
│   └── Range Partitioning.md
├── S/
│   └── Sharding.md
└── V/
    └── Vertical Partitioning.md
```

## Что создано в Inbox

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

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже product-specific overview `PostgreSQL Partitioning`
- [ ] Проверить, когда рядом нужны notes про rebalancing, hot partitions и global indexes
- [ ] Проверить, когда `Sharding` перестает помещаться в одну article-note
- [ ] Подтвердить `section: database-partitioning`
- [ ] Проверить `related`
