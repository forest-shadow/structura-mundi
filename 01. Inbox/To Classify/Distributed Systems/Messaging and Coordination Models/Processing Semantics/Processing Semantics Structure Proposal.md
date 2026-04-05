---
aliases:
  - End-to-End Processing Semantics Structure Proposal
  - Структура ветки Processing Semantics
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Messaging and Coordination Models]]"
status: draft
related:
  - "[[Distributed Systems]]"
  - "[[Messaging and Coordination Models]]"
  - "[[Processing Semantics]]"
  - "[[Event-Driven Architecture]]"
  - "[[Kafka]]"
  - "[[Transactional Outbox]]"
  - "[[Idempotent Consumer]]"
  - "[[Dual Write]]"
tags: []
---

# Processing Semantics Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Processing Semantics` внутри `Messaging and Coordination Models` по правилам `Principia Rerum`.

Для этой ветки не нужно вводить новый `section`:

- `area: computer-science`
- `domain: distributed-systems`
- `section: messaging-and-coordination-models` (переиспользуем существующее значение)

Такое решение лучше, чем заводить отдельный `section: processing-semantics`, потому что речь идет не о новой большой поддисциплине, а об абстрактном кластере гарантий внутри уже существующей ветки messaging and coordination.

## Рекомендуемая иерархия

```text
Distributed Systems (overview)
└── Messaging and Coordination Models (overview)
    ├── Brokered Messaging Model (article)
    ├── Publish-Subscribe (article)
    ├── Producer-Consumer Model (article)
    ├── Gossip Model (article)
    └── Processing Semantics (overview)
        ├── At-Most-Once Delivery (article)
        ├── At-Least-Once Delivery (article)
        ├── Exactly-Once Semantics (article)
        └── Effectively-Once Processing (article)
```

Переиспользуемые соседние заметки:

- `Event-Driven Architecture`
- `Kafka`
- `Transactional Outbox`
- `Idempotent Consumer`
- `Dual Write`

## Почему структура именно такая

- Ваше понятие шире, чем `Kafka delivery semantics`, поэтому его не стоит подчинять продуктовой ветке `Kafka`.
- Каноническое имя `Processing Semantics` лучше, чем `Delivery Semantics`, потому что `delivery` слишком легко читается как гарантия транспорта или брокера, а здесь важна граница всей цепочки `produce -> deliver -> consume -> commit side effect`.
- Формулировку `End-to-End Processing Semantics` лучше сохранить в `aliases`: она полезна как уточнение, но слишком длинна для основного имени обзорной заметки.
- Ветка естественно живет внутри `Messaging and Coordination Models`, потому что описывает не конкретный продукт и не одну архитектурную школу, а абстрактный класс гарантий distributed interaction.
- Один вложенный `overview` здесь оправдан: `at-most-once`, `at-least-once`, `exactly-once` и `effectively-once` образуют устойчивый собственный кластер, а не случайный список отдельных статей.
- `Effectively-Once Processing` полезно держать рядом с `Exactly-Once Semantics`, потому что именно на этом переходе возникает различие между маркетинговой формулой инфраструктуры и реально наблюдаемым итогом на уровне бизнес-цепочки.

## Как лучше понимать терминологию

- `Delivery Semantics` — более узкий слой, обычно про поведение доставки сообщения или записи.
- `Processing Semantics` — более широкий слой, который включает границу обработки, повторной доставки, фиксации результата и побочных эффектов.
- `End-to-End Processing Semantics` — удачное уточнение для случаев, когда нужно явно подчеркнуть, что гарантия оценивается по итоговому наблюдаемому эффекту, а не только по факту передачи сообщения брокером.

Именно поэтому базовый обзорный узел лучше называть `Processing Semantics`, а не `Kafka Delivery Semantics` и не `Exactly-Once Delivery`.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Kafka Delivery Semantics` как родительскую абстрактную рамку для всей темы;
- новый `section: processing-semantics`, если корпус пока ограничен одной компактной подветкой;
- отдельную заметку `Delivery Semantics vs Processing Semantics`, если различие можно четко раскрыть внутри обзорной заметки `Processing Semantics`;
- отдельный `overview` для `Exactly-Once`, если он пока остается одной сложной статьей внутри общего кластера гарантий.

## Предлагаемое физическое размещение после нормализации

Если заметки дойдут до канонического состояния, их физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   ├── At-Least-Once Delivery.md
│   └── At-Most-Once Delivery.md
├── E/
│   ├── Effectively-Once Processing.md
│   └── Exactly-Once Semantics.md
└── P/
    └── Processing Semantics.md
```

Локальные вложения при необходимости:

```text
02. Corpus Mundi/P/_resources/Processing Semantics/
```

## Созданные черновые заметки

- `Processing Semantics.md`
- `At-Most-Once Delivery.md`
- `At-Least-Once Delivery.md`
- `Exactly-Once Semantics.md`
- `Effectively-Once Processing.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Проверить, достаточно ли `Processing Semantics` как канонического имени, или позднее понадобится более узкая статья `Delivery Semantics`.
2. Решить, когда рядом нужен product-specific article `Kafka Delivery Semantics`.
3. Уточнить границу между `Exactly-Once Semantics` как инфраструктурной формулой и `Effectively-Once Processing` как end-to-end практикой.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
