# Transaction Isolation Levels Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Transaction Isolation Levels` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее предлагается новое значение `section`:

- `area: computer-science`
- `domain: databases`
- `section: transactions` (предлагаемое новое значение)

`domain` уже существует в словаре. Новым здесь является только `section`, и его имеет смысл вводить не ради одной заметки, а ради устойчивого кластера тем о транзакциях в базах данных.

## Рекомендуемая иерархия

```text
Database Transactions (overview)
├── ACID (article)
└── Transaction Isolation Levels (overview)
    ├── Isolation Anomalies (article)
    ├── Read Uncommitted (article)
    ├── Read Committed (article)
    ├── Repeatable Read (article)
    ├── Serializable (article)
    └── Snapshot Isolation (article)
```

## Почему структура именно такая

- `Transaction Isolation Levels` достаточно велика, чтобы быть отдельным `overview`, а не одной длинной статьей.
- Вложенный `overview` здесь оправдан, потому что у темы есть собственное устойчивое поддерево: уровни изоляции, аномалии и связанные механизмы.
- Более широкий узел `Database Transactions` полезен как родительская рамка, потому что рядом с изоляцией естественно живут `ACID`, concurrency concerns и другие темы про транзакции.
- Глубже ветку сейчас дробить не нужно: отдельные уровни изоляции уже достаточно оформлять как плоские `article`.
- Отдельный `sub-overview` для аномалий или для snapshot-based моделей пока избыточен.

## Что пока не нужно создавать

Пока не стоит заранее заводить отдельные узлы:

- `Concurrency Control` как отдельный `overview`, если тема пока не разрослась в самостоятельную ветку;
- `Lock-Based Concurrency Control` как дочернюю ветку внутри `Transaction Isolation Levels`;
- отдельные статьи для `Dirty Read`, `Non-Repeatable Read`, `Phantom Read`, если пока достаточно обзорной заметки `Isolation Anomalies`;
- вторую параллельную ветку `MVCC`, если заметка пока нужна только как смежное понятие, а не как самостоятельный кластер.

## Предлагаемое физическое размещение после нормализации

Если `section` будет утвержден и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   └── ACID.md
├── D/
│   └── Database Transactions.md
├── I/
│   └── Isolation Anomalies.md
├── R/
│   ├── Read Committed.md
│   ├── Read Uncommitted.md
│   └── Repeatable Read.md
├── S/
│   ├── Serializable.md
│   └── Snapshot Isolation.md
└── T/
    └── Transaction Isolation Levels.md
```

Это важно: логическая иерархия задается через `parent` и ссылки, а не через физическую близость файлов.

## Созданные черновые заметки

- `Database Transactions.md`
- `ACID.md`
- `Transaction Isolation Levels.md`
- `Isolation Anomalies.md`
- `Read Uncommitted.md`
- `Read Committed.md`
- `Repeatable Read.md`
- `Serializable.md`
- `Snapshot Isolation.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: transactions` как рабочий тематический кластер внутри `domain: databases`.
2. Решить, нужно ли в этом же кластере дальше заводить `MVCC` и `Concurrency Control` как соседние статьи или отдельную подветку.
3. Уточнить, достаточно ли одной статьи `Isolation Anomalies`, или позже стоит разносить аномалии на отдельные заметки.
4. После этого перевести заметки из `seed` в содержательные черновики и наполнить их материалом.
