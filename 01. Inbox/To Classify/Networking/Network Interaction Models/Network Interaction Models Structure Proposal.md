# Network Interaction Models Structure Proposal

## Краткое определение

Предлагаемое место для `Network Interaction Models` внутри `Networking` как обзорной ветки для базовых форм сетевого взаимодействия.

## Рекомендуемая иерархия

```text
Networking
└── Network Interaction Models
    ├── Client-Server Model
    ├── Peer-to-Peer Model
    ├── Request-Reply Model
    └── Broadcast and Multicast Model
```

## Почему структура именно такая

- Эти заметки находятся на одном уровне абстракции: они описывают форму сетевого взаимодействия между узлами, а не messaging middleware или distributed coordination.
- `Client-Server Model` больше не должна быть единственным model-centric узлом напрямую под `Networking`, потому что рядом появились равноправные sibling-модели.
- `Request-Reply Model` и `Client-Server Model` нужно держать как соседние, а не как отношение родитель-дочерний узел: они тесно связаны, но не сводятся друг к другу.

## Что не стоит делать прямо сейчас

- Не стоит включать сюда `Publish-Subscribe`, `Producer-Consumer` или `Gossip`, потому что эти темы уже выходят на уровень distributed interaction patterns.
- Не стоит смешивать interaction models с protocol families или topology notes.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `Anycast` и `Unicast`
- [ ] Проверить будущие `related` с `Distributed Systems`



