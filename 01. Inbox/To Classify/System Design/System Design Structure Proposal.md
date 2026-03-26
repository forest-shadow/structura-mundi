# System Design Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для ветки `System Design` внутри `Computer Science` по правилам `Principia Rerum`.

На текущем этапе ветка уже оправдана не только через `Service Reliability`, но и через отдельные кластеры про проектные принципы и управление зависимостями.

## Рекомендуемая иерархия

```text
Computer Science
└── System Design
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
    └── Service Reliability
```

Соседняя language-specific заметка:

- `Composition Root in Go`

## Почему структура именно такая

- `Design Principles` и `Dependency Management` полезно разводить, потому что первое отвечает за нормативные идеи, а второе за практики организации кода и зависимостей.
- `SOLID` естественно живет под `Design Principles`, а не под `Dependency Management`.
- `Dependency Inversion Principle` концептуально связан с `Dependency Injection` и `Composition Root`, но не тождествен им.
- `Composition Root` лучше рассматривать как дочернюю тему `Dependency Injection`: это не отдельный принцип, а место и практика сборки приложения.
- `Service Locator` стоит рядом с `Dependency Injection`, потому что это соседний способ доступа к зависимостям, обычно менее желательный.
- `Composition Root in Go` не должен становиться отдельным корнем внутри `System Design`, потому что это языковая реализация общей архитектурной идеи.

## Что не нужно создавать заранее

- отдельный domain-root `Software Architecture`, если ветка пока естественно встраивается в `System Design`;
- отдельную обзорную заметку `Bootstrap`, если она нужна только как синоним composition root;
- отдельную заметку `Dependency Injection Container`, пока нет корпуса по контейнерам как самостоятельной теме.

## Следующий шаг

1. Подтвердить, что `Design Principles` и `Dependency Management` получают собственные `section`.
2. Наполнить `SOLID` и `Dependency Injection` краткими каноническими определениями.
3. Позже решить, нужен ли отдельный узел про `Hexagonal Architecture` или `Ports and Adapters`.
