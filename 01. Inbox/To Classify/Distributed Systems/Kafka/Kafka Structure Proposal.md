
# Kafka Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Kafka` в контексте распределенных систем по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется новое значение `section`:

- `area: computer-science`
- `domain: distributed-systems`
- `section: kafka` (предлагаемое новое значение)

`domain` уже существует в словаре, а `section` еще нужно отдельно утвердить перед переносом ветки в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
Distributed Systems (overview)
└── Kafka (overview)
    ├── Kafka Topic (article)
    ├── Kafka Partition (article)
    ├── Kafka Consumer Group (article)
    ├── Kafka Offset (article)
    └── Kafka Delivery Semantics (overview)
        ├── Kafka At-Most-Once Delivery (article)
        ├── Kafka At-Least-Once Delivery (article)
        └── Kafka Exactly-Once Semantics (article)
```

Соседние переиспользуемые заметки:

- `Brokered Messaging Model`
- `Message Broker`
- `Publish-Subscribe`
- `Producer-Consumer Model`
- `Transactional Outbox`

## Почему структура именно такая

- `Kafka` лучше оформлять как отдельный `overview`, а не как обычную article-note, потому что вокруг него естественно собирается устойчивый product-specific кластер заметок про topics, partitions, consumer groups, offsets, delivery semantics и operational behavior.
- Ветка логичнее живет внутри `Distributed Systems`, а не внутри `Databases`: Kafka здесь важен прежде всего как распределенная платформа передачи и хранения событийного потока, а не как database-specific тема.
- `Kafka` не стоит подчинять `Brokered Messaging Model`, потому что эта заметка описывает более абстрактный interaction pattern, тогда как Kafka одновременно пересекается с brokered messaging, publish-subscribe, producer-consumer и event streaming.
- `Kafka Topic`, `Kafka Partition`, `Kafka Consumer Group` и `Kafka Offset` дают минимальный каркас для большинства последующих заметок о Kafka и позволяют теперь уже осмысленно подвесить подветку `Kafka Delivery Semantics`.
- Отдельный `sub-overview` `Kafka Delivery Semantics` теперь оправдан, потому что внутри него появляется не одна статья, а устойчивое поддерево из трех различимых режимов доставки.
- При этом глубже ветку дробить пока не нужно: подузлы вроде `Kafka Storage Model` или `Kafka Internals` все еще будут преждевременными.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Event Streaming Platform` как дополнительный абстрактный уровень только ради одного продукта;
- `Kafka Broker`, если еще нет корпуса заметок про cluster internals, replication, leader election и controller mechanics;
- `Kafka Producer Idempotence` как отдельный обзорный узел, если пока это лишь механизм внутри статьи про `Kafka Exactly-Once Semantics`;
- `Kafka Transactions` как отдельную подветку, если рядом еще нет устойчивого корпуса заметок про transactional producer и stream-processing choreography;
- отдельные template-файлы под Kafka-ветку, потому что по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

Если `section` будет утвержден и заметки дойдут до канонического состояния, их физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── K/
    ├── Kafka.md
    ├── Kafka At-Least-Once Delivery.md
    ├── Kafka At-Most-Once Delivery.md
    ├── Kafka Consumer Group.md
    ├── Kafka Delivery Semantics.md
    ├── Kafka Exactly-Once Semantics.md
    ├── Kafka Offset.md
    ├── Kafka Partition.md
    └── Kafka Topic.md
```

Локальные вложения при необходимости:

```text
02. Corpus Mundi/K/_resources/Kafka/
```

## Созданные черновые заметки

- `Kafka.md`
- `Kafka Topic.md`
- `Kafka Partition.md`
- `Kafka Consumer Group.md`
- `Kafka Offset.md`
- `Kafka Delivery Semantics.md`
- `Kafka At-Most-Once Delivery.md`
- `Kafka At-Least-Once Delivery.md`
- `Kafka Exactly-Once Semantics.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: kafka`.
2. Проверить, не нужен ли позже отдельный overview-узел для Kafka internals или для механизмов вроде producer idempotence и transactions.
3. Проверить границу между `Kafka` как product-веткой и `Messaging and Coordination Models` как абстрактной веткой паттернов.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
