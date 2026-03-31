# Software Architecture Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для ветки `Software Architecture` внутри `Computer Science` по правилам `Principia Rerum`.

На текущем этапе ветка оправдана отдельными кластерами про проектные принципы, управление зависимостями и устойчивые архитектурные стили.

## Рекомендуемая иерархия

```text
Computer Science
└── Software Architecture
    ├── Design Principles
    │   └── SOLID
    │       ├── Single Responsibility Principle
    │       ├── Open-Closed Principle
    │       ├── Liskov Substitution Principle
    │       ├── Interface Segregation Principle
    │       └── Dependency Inversion Principle
    ├── Dependency Management
    │   ├── Inversion of Control
    │   ├── Dependency Injection
    │   │   └── Composition Root
    │   └── Service Locator
    ├── Clean Architecture
    └── Connection Pooling
```

Соседние cross-domain и language-specific заметки:

- `Composition Root in Go`
- `Database Connection Pooling`

## Почему структура именно такая

- `Design Principles` и `Dependency Management` полезно разводить, потому что первое отвечает за нормативные идеи, а второе за практики организации кода и зависимостей.
- `SOLID` естественно живет под `Design Principles`, а не под `Dependency Management`.
- `Dependency Inversion Principle` концептуально связан с `Dependency Injection` и `Composition Root`, но не тождествен им.
- `Composition Root` лучше рассматривать как дочернюю тему `Dependency Injection`: это не отдельный принцип, а место и практика сборки приложения.
- `Service Locator` стоит рядом с `Dependency Injection`, потому что это соседний способ доступа к зависимостям, обычно менее желательный.
- `Connection Pooling` лучше держать в `Software Architecture` как общую инженерную статью о паттерне reuse соединений, а не в `Databases`, потому что тема шире database-specific контекста.
- `Database Connection Pooling` при этом не должно становиться дочерней статьей `Connection Pooling`: это соседняя прикладная database-specific статья, связанная через `related`.
- `Composition Root in Go` не должен становиться отдельным корнем внутри `Software Architecture`, потому что это языковая реализация общей архитектурной идеи.
- `Service Reliability` лучше держать в `Distributed Systems`, потому что это ветка про эксплуатацию и надежность распределенных сервисов, а не про общие архитектурные практики.

## Что не нужно создавать заранее

- отдельную обзорную заметку `Bootstrap`, если она нужна только как синоним composition root;
- отдельную заметку `Dependency Injection Container`, пока нет корпуса по контейнерам как самостоятельной теме.

## Следующий шаг

1. Подтвердить, что `Design Principles` и `Dependency Management` получают собственные `section`.
2. Наполнить `SOLID` и `Dependency Injection` краткими каноническими определениями.
3. Позже решить, нужен ли отдельный узел про `Hexagonal Architecture` или `Ports and Adapters`.
