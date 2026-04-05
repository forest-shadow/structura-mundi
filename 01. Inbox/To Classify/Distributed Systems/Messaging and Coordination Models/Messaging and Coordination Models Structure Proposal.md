# Messaging and Coordination Models Structure Proposal

## Краткое определение

Предлагаемое место для `Messaging and Coordination Models` внутри `Distributed Systems` как обзорной ветки для более абстрактных distributed interaction patterns.

## Рекомендуемая иерархия

```text
Distributed Systems
└── Messaging and Coordination Models
    ├── Brokered Messaging Model
    ├── Publish-Subscribe
    ├── Producer-Consumer Model
    ├── Gossip Model
    └── Processing Semantics
        ├── At-Most-Once Delivery
        ├── At-Least-Once Delivery
        ├── Exactly-Once Semantics
        └── Effectively-Once Processing
```

## Почему структура именно такая

- Эти заметки уже находятся на более высоком уровне, чем чистые network interaction models: здесь важны посредники, temporal decoupling, независимые consumers и распространение состояния.
- `Publish-Subscribe` не должен оставаться только дочерней заметкой `Event-Driven Architecture`, если он используется как более общий distributed interaction pattern.
- `Brokered Messaging Model`, `Producer-Consumer Model` и `Gossip Model` естественно читаются рядом друг с другом как формы координации и доставки в распределенной системе.
- `Processing Semantics` стоит оформить как вложенный `overview`, потому что at-most-once, at-least-once, exactly-once и effectively-once образуют отдельный устойчивый кластер гарантий, который уже шире одного продукта вроде Kafka.

## Что не стоит делать прямо сейчас

- Не стоит смешивать эту ветку с `Networking`: там остаются interaction models уровня client-server, peer-to-peer, request-reply и broadcast/multicast.
- Не стоит насильно сводить всю ветку к `Event-Driven Architecture`: EDA остается соседней архитектурной рамкой, а не контейнером для всех messaging patterns.
- Не стоит уводить эту тему в `Kafka`, если речь идет об абстрактных end-to-end гарантиях, а не о product-specific semantics.

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: messaging-and-coordination-models`
- [ ] Решить, когда рядом нужны `Work Queue Model` и `Message-Driven Architecture`
- [ ] Проверить, не нужен ли позже отдельный article `Kafka Delivery Semantics`
