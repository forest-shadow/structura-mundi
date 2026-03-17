# Distributed Systems Problems Structure Proposal

## Назначение

Этот файл фиксирует минимальную обзорную заготовку для темы `Distributed Systems Problems` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется новое значение `section`:

- `area: computer-science`
- `domain: distributed-systems`
- `section: distributed-systems-problems` (предлагаемое новое значение)

Эта ветка нужна не как энциклопедия всех проблем распределенных систем сразу, а как обзорная рамка, в которую можно постепенно вкладывать реальные подветки.

## Рекомендуемая иерархия на текущем этапе

```text
Distributed Systems Problems (overview)
├── Partial Failure (overview)
├── Time and Ordering (overview)
├── Coordination and Consensus (overview)
├── Consistency Under Replication (overview)
└── Dual Write (overview)
    ├── Polling Publisher (article)
    ├── Change Data Capture (article)
    └── Distributed Transaction (article)
```

Соседняя переиспользуемая заметка:

- `Transactional Outbox`

## Почему структура именно такая

- `Distributed Systems Problems` дает обзорную картину и позволяет привязывать частные проблемы к более общей рамке.
- Четыре новые ветки представляют устойчивые problem-centered кластеры, которые полезны для навигации уже сейчас.
- `Dual Write` уже достаточно оформлен как самостоятельная подветка и поэтому должен жить под этой обзорной темой как дочерний `overview`.
- Глубже дерево пока не нужно усложнять: на этом этапе достаточно только обзорных узлов без новой глубокой вложенности.

## Какие ветки уже стоит зафиксировать

На текущем этапе уже оправдано создать обзорные узлы:

- `Partial Failure`
- `Time and Ordering`
- `Coordination and Consensus`
- `Consistency Under Replication`

Эти ветки уже достаточно устойчивы концептуально и полезны как рамка для будущих заметок.

## Предлагаемое физическое размещение после нормализации

Если `section` будет утвержден и обзорная ветка дойдет до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── C/
│   ├── Consistency Under Replication.md
│   └── Coordination and Consensus.md
├── D/
│   └── Distributed Systems Problems.md
├── P/
│   └── Partial Failure.md
└── T/
    └── Time and Ordering.md
```

Дочерние тематические ветки при этом могут жить в своих буквенных папках:

```text
02. Corpus Mundi/
├── D/
│   ├── Distributed Systems Problems.md
│   └── Dual Write.md
├── C/
│   └── Change Data Capture.md
└── P/
    └── Polling Publisher.md
```

## Созданные и привязанные заметки

- `Distributed Systems Problems.md`
- `Partial Failure.md`
- `Time and Ordering.md`
- `Coordination and Consensus.md`
- `Consistency Under Replication.md`
- `Dual Write.md` как дочерний `overview`

## Следующий шаг

1. Подтвердить `section: distributed-systems-problems`.
2. Решить, какие первые дочерние article появятся внутри `Partial Failure`, `Time and Ordering`, `Coordination and Consensus`, `Consistency Under Replication`.
3. Не добавлять новые подветки без содержательного наполнения.
