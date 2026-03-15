# Event-Driven Architecture Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Event-Driven Architecture` в контексте распределенных систем по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется новое значение `section`:

- `area: computer-science`
- `domain: distributed-systems`
- `section: event-driven-architecture` (предлагаемое новое значение)

`domain` уже существует в словаре, а `section` еще нужно отдельно утвердить перед переносом ветки в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
Event-Driven Architecture (overview)
├── Event Collaboration Patterns (overview)
│   ├── Event Notification (article)
│   ├── Event-Carried State Transfer (article)
│   └── Competing Consumers (article)
├── Publish-Subscribe (article)
├── Message Broker (article)
├── Transactional Outbox (article)
└── Idempotent Consumer (article)
```

## Почему структура именно такая

- `Event-Driven Architecture` является естественной канонической обзорной точкой входа для всей ветки.
- Один вложенный `overview` для `Event Collaboration Patterns` оправдан, потому что внутри EDA есть отдельный устойчивый кластер паттернов взаимодействия между сервисами.
- `Publish-Subscribe`, `Message Broker`, `Transactional Outbox` и `Idempotent Consumer` пока лучше держать как обычные `article`, а не раздувать дерево еще одним уровнем вложенности.
- Структура остается достаточно плоской и соответствует правилу минимальной вложенности.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Distributed Systems` как новый обзорный слой только ради размещения EDA;
- `Asynchronous Communication` как обязательный промежуточный уровень;
- отдельные обзорные ветки для `CQRS`, `Event Sourcing`, `Saga`, `Stream Processing`, если по ним еще нет самостоятельного корпуса;
- отдельную заметку `Event`, если пока не требуется собственная энциклопедическая статья с четкими границами.

Эти темы можно добавить позже как соседние ветки или связанные `article`, если корпус вырастет.

## Предлагаемое физическое размещение после нормализации

Если `section` будет утвержден и заметки дойдут до канонического состояния, их физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── C/
│   └── Competing Consumers.md
├── E/
│   ├── Event-Driven Architecture.md
│   ├── Event Collaboration Patterns.md
│   ├── Event Notification.md
│   └── Event-Carried State Transfer.md
├── I/
│   └── Idempotent Consumer.md
├── M/
│   └── Message Broker.md
├── P/
│   └── Publish-Subscribe.md
└── T/
    └── Transactional Outbox.md
```

Локальные вложения при необходимости:

```text
02. Corpus Mundi/E/_resources/Event-Driven Architecture/
```

## Созданные черновые заметки

- `Event-Driven Architecture.md`
- `Event Collaboration Patterns.md`
- `Event Notification.md`
- `Event-Carried State Transfer.md`
- `Competing Consumers.md`
- `Publish-Subscribe.md`
- `Message Broker.md`
- `Transactional Outbox.md`
- `Idempotent Consumer.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: event-driven-architecture`.
2. Проверить, не стоит ли часть тем позднее выделить в соседние ветки, а не держать внутри EDA.
3. Решить, нужны ли для этой ветки отдельные заметки `CQRS`, `Event Sourcing` и `Saga` как связанные, но не дочерние темы.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
