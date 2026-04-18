---
aliases:
  - UML Branch Structure Proposal
  - Структура ветки UML
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[Software Architecture]]"
status: draft
related:
  - "[[Software Architecture]]"
  - "[[UML]]"
  - "[[UML Structural Diagrams]]"
  - "[[UML Behavioral Diagrams]]"
  - "[[Clean Architecture]]"
tags: []
---

# UML Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для ветки `UML`, в которую естественно помещается рассмотрение такого понятия, как `UML`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: software-architecture`
- `section: architecture-modeling`

Почему так:

- `UML` в этом vault логичнее всего рассматривать как язык архитектурного и проектного моделирования, а не как паттерн, принцип или language-specific прием;
- существующие `section` внутри `software-architecture` не подходят точно: `architecture-patterns` описывает устойчивые решения, `design-principles` - нормативные идеи, `dependency-management` - wiring зависимостей, `performance-modeling` - математические модели нагрузки;
- новый `section: architecture-modeling` полезен не для одной заметки, а для серии соседних notes про UML, диаграммы и возможные будущие ветки вроде `C4 Model`.

## Канонические имена

- overview: `UML`
- sub-overview:
  - `UML Structural Diagrams`
  - `UML Behavioral Diagrams`
- articles:
  - `UML Class Diagram`
  - `UML Component Diagram`
  - `UML Deployment Diagram`
  - `UML Use Case Diagram`
  - `UML Sequence Diagram`
  - `UML Activity Diagram`
  - `UML State Machine Diagram`

## Рекомендуемая иерархия

```text
Software Architecture
└── UML
    ├── UML Structural Diagrams
    │   ├── UML Class Diagram
    │   ├── UML Component Diagram
    │   └── UML Deployment Diagram
    └── UML Behavioral Diagrams
        ├── UML Use Case Diagram
        ├── UML Sequence Diagram
        ├── UML Activity Diagram
        └── UML State Machine Diagram
```

## Почему структура именно такая

- `UML` лучше сделать `overview`, потому что это не один механизм, а целый язык моделирования с устойчивым набором дочерних диаграмм.
- Деление на `UML Structural Diagrams` и `UML Behavioral Diagrams` стоит вынести в `sub-overview`, потому что это каноническая граница внутри самой темы, а не случайная редакторская группировка.
- `UML Class Diagram`, `UML Component Diagram` и `UML Deployment Diagram` лучше держать как отдельные `article`, потому что каждая диаграмма отвечает на собственный тип архитектурного вопроса.
- `UML Use Case Diagram`, `UML Sequence Diagram`, `UML Activity Diagram` и `UML State Machine Diagram` также заслуживают отдельных статей: это не подпункты одной страницы, а самостоятельные формы описания поведения.
- Не стоит сейчас вводить еще один уровень над `UML`, например `Software Modeling`, потому что для него пока нет корпуса sibling-веток; по `Principia Rerum` это было бы преждевременным усложнением.

## Что не стоит делать прямо сейчас

- Не стоит помещать `UML` под `Design Principles`: язык моделирования не является принципом проектирования.
- Не стоит помещать `UML` под `Clean Architecture`: архитектурная рамка и язык описания системы - разные уровни.
- Не стоит создавать отдельные тематические template-файлы под UML-ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`, развернутых в конкретные заметки ветки.
- Не стоит заранее заводить отдельные заметки про каждую нотационную деталь вроде `Multiplicity`, `Aggregation` или `Lifeline`, пока рядом нет полноценного корпуса diagram-specific материалов.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── U/
    ├── UML.md
    ├── UML Structural Diagrams.md
    ├── UML Class Diagram.md
    ├── UML Component Diagram.md
    ├── UML Deployment Diagram.md
    ├── UML Behavioral Diagrams.md
    ├── UML Use Case Diagram.md
    ├── UML Sequence Diagram.md
    ├── UML Activity Diagram.md
    └── UML State Machine Diagram.md
```

## Что уже создано в Inbox

- `[[UML]]`
- `[[UML Structural Diagrams]]`
- `[[UML Component Diagram]]`
- `[[UML Deployment Diagram]]`
- `[[UML Class Diagram]]`
- `[[UML Behavioral Diagrams]]`
- `[[UML Use Case Diagram]]`
- `[[UML Sequence Diagram]]`
- `[[UML Activity Diagram]]`
- `[[UML State Machine Diagram]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `UML` нужен `C4 Model` как sibling-ветка, а не как дочерняя статья
- [ ] Проверить границы между `UML Component Diagram` и общими архитектурными рамками вроде `Clean Architecture`
- [ ] Проверить, нужен ли позже отдельный узел про diagram notation basics
- [ ] Проверить `related`
