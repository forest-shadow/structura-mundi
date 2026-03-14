# Dual Write Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Dual Write` в контексте распределенных систем по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется новое значение `section`:

- `area: computer-science`
- `domain: distributed-systems`
- `section: dual-write` (предлагаемое новое значение)

`domain` уже существует в словаре, а `section` еще нужно отдельно утвердить перед переносом ветки в `02. Corpus Mundi`.

## Рекомендуемая иерархия

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

- `Dual Write` является естественной канонической обзорной точкой входа для самой проблемы рассогласования между локальным состоянием и публикацией внешнего эффекта.
- При этом полезно рассматривать ее внутри более общей обзорной рамки `Distributed Systems Problems`, чтобы формировалась карта более широкого класса проблем.
- Ветка не требует вложенного `overview`, потому что у нее нет крупного самостоятельного поддерева.
- `Polling Publisher`, `Change Data Capture` и `Distributed Transaction` достаточно оформить как плоские `article`.
- `Transactional Outbox` не нужно создавать повторно, потому что он уже существует как соседняя заметка в ветке EDA и должен переиспользоваться как общее решение, а не клонироваться в разных местах.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Consistency Between State and Messages` как дополнительный абстрактный уровень;
- `Exactly-Once Delivery` как дочернюю тему внутри `Dual Write`;
- отдельный `overview` для `Transactional Outbox`, если он уже живет как самостоятельная статья;
- отдельную ветку по `Saga`, если речь пока идет именно о согласовании локальной записи и публикации события.

## Предлагаемое физическое размещение после нормализации

Если `section` будет утвержден и заметки дойдут до канонического состояния, их естественное размещение:

```text
02. Corpus Mundi/
└── D/
    ├── Dual Write.md
    ├── Polling Publisher.md
    ├── Change Data Capture.md
    └── Distributed Transaction.md
```

При этом `Transactional Outbox` должен остаться одной канонической заметкой и быть связан через `related`, а не размножаться по нескольким папкам.

Локальные вложения при необходимости:

```text
02. Corpus Mundi/D/_resources/Dual Write/
```

## Созданные черновые заметки

- `Dual Write.md`
- `Polling Publisher.md`
- `Change Data Capture.md`
- `Distributed Transaction.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: dual-write`.
2. Подтвердить обзорную рамку `Distributed Systems Problems` как родительскую для `Dual Write`.
3. Решить, должна ли `Transactional Outbox` считаться дочерней темой `Dual Write` или общей переиспользуемой статьей на пересечении EDA и consistency concerns.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
