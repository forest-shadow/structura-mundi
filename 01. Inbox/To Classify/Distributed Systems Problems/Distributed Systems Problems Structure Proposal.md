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
└── Dual Write (overview)
    ├── Polling Publisher (article)
    ├── Change Data Capture (article)
    └── Distributed Transaction (article)
```

Соседняя переиспользуемая заметка:

- `Transactional Outbox`

## Почему структура именно такая

- `Distributed Systems Problems` дает обзорную картину и позволяет привязывать частные проблемы к более общей рамке.
- `Dual Write` уже достаточно оформлен как самостоятельная подветка и поэтому должен жить под этой обзорной темой как дочерний `overview`.
- Глубже дерево пока не нужно усложнять.
- Остальные большие кластеры проблем лучше добавлять только по мере появления реального корпуса заметок.

## Какие будущие ветки здесь могут появиться

Позже здесь могут появиться соседние узлы вроде:

- `Partial Failure`
- `Time and Ordering`
- `Consistency Under Replication`
- `Coordination and Consensus`

Но сейчас их не нужно заводить автоматически, чтобы не строить пустую и слишком абстрактную схему.

## Предлагаемое физическое размещение после нормализации

Если `section` будет утвержден и обзорная ветка дойдет до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── D/
    └── Distributed Systems Problems.md
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
- `Dual Write.md` как дочерний `overview`

## Следующий шаг

1. Подтвердить `section: distributed-systems-problems`.
2. Решить, какие следующие реальные проблемы распределенных систем заслуживают собственных заметок.
3. Не добавлять новые подветки без содержательного наполнения.
