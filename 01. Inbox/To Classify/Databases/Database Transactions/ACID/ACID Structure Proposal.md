---
aliases: []
note_type: article
area: computer-science
domain: databases
section: transactions
parent: "[[Database Transactions]]"
status: draft
related:
  - "[[Database Transactions]]"
  - "[[ACID]]"
  - "[[Transaction Isolation Levels]]"
tags:
  - transactions
  - consistency
---

# ACID Structure Proposal

## Краткое определение

Предлагаемая структура для `ACID` делает сам акроним обзорным узлом, а каждое его свойство отдельным каноническим объектом знания.

## Почему текущего состояния недостаточно

- В существующей `[[ACID]]` уже описаны `Atomicity`, `Consistency`, `Isolation` и `Durability`, но они пока не вынесены в отдельные канонические заметки.
- Это мешает ссылаться на отдельные свойства транзакций как на самостоятельные объекты знания.
- Особенность `Isolation` требует собственной обзорной ветки, потому что она естественно связывается с `[[Transaction Isolation Levels]]`.

## Предлагаемая логическая структура

- `[[Database Transactions]]`
- `[[ACID]]`
- `[[Transaction Atomicity]]`
- `[[Transaction Consistency]]`
- `[[Transaction Isolation]]`
- `[[Transaction Isolation Levels]]`
- `[[Transaction Durability]]`

## Предлагаемая иерархия

```text
Database Transactions
└── ACID
    ├── Transaction Atomicity
    ├── Transaction Consistency
    ├── Transaction Isolation
    │   └── Transaction Isolation Levels
    └── Transaction Durability
```

## Почему именно так

- `ACID` становится `overview`, потому что собирает четыре свойства в одну осмысленную ветку.
- Для дочерних заметок используются уточнённые имена `Transaction ...`, чтобы не смешивать их с более общими понятиями `Consistency`, `Isolation` или `Durability` в других областях.
- Дополнительная вложенность появляется только у `[[Transaction Isolation]]`, потому что у него уже есть реальная дочерняя обзорная ветка `[[Transaction Isolation Levels]]`.
- Остальные свойства остаются обычными `article`, чтобы не раздувать глубину структуры без необходимости.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── ACID.md
└── T/
    ├── Transaction Atomicity.md
    ├── Transaction Consistency.md
    ├── Transaction Isolation.md
    ├── Transaction Isolation Levels.md
    └── Transaction Durability.md
```

## Что уже создано в Inbox

- `[[ACID]]` переопределена как `overview`
- `[[Transaction Atomicity]]`
- `[[Transaction Consistency]]`
- `[[Transaction Isolation]]`
- `[[Transaction Durability]]`

## Что стоит раскрыть дальше

- [ ] Перенести краткие определения из `[[ACID]]` в дочерние заметки
- [ ] Уточнить границы `Transaction Consistency` и не смешивать её с CAP-consistency
- [ ] Связать `Transaction Isolation` с `[[Isolation Anomalies]]`
- [ ] Решить, нужны ли отдельные статьи про WAL и concurrency control в этой же ветке или как соседние ветки
