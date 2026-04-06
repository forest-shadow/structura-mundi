---
aliases:
  - PostgreSQL Structure Proposal
  - Структура ветки PostgreSQL
note_type: article
area: computer-science
domain: databases
section: postgresql
parent: "[[Databases]]"
status: draft
related:
  - "[[Databases]]"
  - "[[PostgreSQL]]"
  - "[[PostgreSQL Architecture]]"
  - "[[PostgreSQL Transaction Isolation]]"
  - "[[Transaction Isolation Levels]]"
tags: []
---

# PostgreSQL Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `PostgreSQL`, включая PostgreSQL-specific рассмотрение уровней изоляции транзакций, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: databases`
- `section: postgresql` (предлагаемое рабочее значение)

Почему так:

- `PostgreSQL` естественно ложится в уже существующий `domain: databases`, а не требует отдельного домена;
- рядом с `PostgreSQL` уже естественно возникают product-specific темы про архитектуру сервера и семантику транзакционной изоляции;
- отдельный `section: postgresql` оправдан, потому что тема не сводится к одной статье и не должна растворяться среди общих database notes.

## Канонические имена

- section-level overview: `PostgreSQL`
- article: `PostgreSQL Architecture`
- article: `PostgreSQL Transaction Isolation`

Форму `Postgres` лучше хранить в `aliases`, а не делать отдельным каноническим файлом, если речь идет о той же самой продуктовой ветке.

## Рекомендуемая иерархия

```text
Databases
└── PostgreSQL
    ├── PostgreSQL Architecture
    └── PostgreSQL Transaction Isolation
```

## Почему структура именно такая

- `PostgreSQL` лучше делать `overview`, потому что это уже не один частный термин, а устойчивый product-specific узел.
- `PostgreSQL Architecture` нужен отдельной `article`, потому что архитектурная модель сервера, процессов, shared buffers, WAL и query execution — это самостоятельный аспект продукта.
- `PostgreSQL Transaction Isolation` тоже нужен отдельной `article`, потому что PostgreSQL-specific поведение уровней изоляции нельзя аккуратно растворить ни в общей статье `Transaction Isolation Levels`, ни в общей product overview.
- При этом не стоит дублировать всю общую transactional ветку внутри PostgreSQL: product-specific note должна ссылаться на `[[Transaction Isolation Levels]]`, а не копировать её дерево под другим именем.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельный `sub-overview` вроде `PostgreSQL Internals`, пока рядом всего несколько стартовых PostgreSQL-specific notes.
- Не стоит заводить отдельные заметки `PostgreSQL Read Committed`, `PostgreSQL Repeatable Read` и `PostgreSQL Serializable`, пока эти различия естественно помещаются в одну статью `PostgreSQL Transaction Isolation`.
- Не стоит создавать специальные template-файлы под `PostgreSQL`: по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── P/
    ├── PostgreSQL.md
    ├── PostgreSQL Architecture.md
    └── PostgreSQL Transaction Isolation.md
```

## Что уже создано в Inbox

- `[[PostgreSQL]]`
- `[[PostgreSQL Architecture]]`
- `[[PostgreSQL Transaction Isolation]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны отдельные notes про MVCC, WAL и vacuum
- [ ] Проверить, когда `PostgreSQL Transaction Isolation` перестает помещаться в одну статью
- [ ] Подтвердить `section: postgresql`
- [ ] Проверить `related`