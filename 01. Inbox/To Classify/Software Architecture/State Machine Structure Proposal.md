---
aliases:
  - State Machine Branch Structure Proposal
  - Структура заметки State Machine
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[Software Architecture]]"
status: draft
related:
  - "[[Software Architecture]]"
  - "[[State Machine]]"
  - "[[Finite Automaton]]"
  - "[[UML State Machine Diagram]]"
  - "[[Event-Driven Architecture]]"
tags: []
---

# State Machine Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `State Machine`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: software-architecture`
- `section: architecture-modeling`
- `parent: [[Software Architecture]]`

Почему так:

- здесь `State Machine` рассматривается не как строгий формальный автомат из теории языков, а как инженерная модель поведения системы через состояния, события и переходы;
- существующий `section: architecture-modeling` уже подходит для behavioral-моделей и не требует расширения словаря;
- formal-theory ближайший узел уже существует в другой ветке как `[[Finite Automaton]]`, поэтому дублировать его внутри `software-architecture` не нужно;
- `UML State Machine Diagram` тоже уже существует, но это именно способ нотации и визуализации, а не вся тема state-machine modeling.

## Каноническое имя

- корневая заметка: `State Machine`

## Рекомендуемая иерархия

```text
Software Architecture
└── State Machine
```

Поперечные связи:

```text
State Machine ↔ Finite Automaton
State Machine ↔ UML State Machine Diagram
State Machine ↔ Event-Driven Architecture
```

## Почему структура именно такая

- `State Machine` лучше сделать обычной `article`, а не `overview`, потому что на текущем этапе рядом еще нет устойчивого корпуса дочерних заметок.
- Тему не стоит подчинять `UML`, потому что UML-диаграмма выражает state machine графически, но не исчерпывает сам инженерный концепт.
- Тему не стоит переносить в `Automata Theory`, потому что там уже живет строгая формальная модель `Finite Automaton` и другой дисциплинарный фокус.
- Если позже корпус вырастет, рядом можно будет естественно добавить `Hierarchical State Machine`, `Statechart` или `Extended State Machine`, но пока делать это заранее не нужно.

## Что не стоит делать прямо сейчас

- Не стоит заводить отдельную заметку `Finite State Machine` внутри `Software Architecture`: в строгом смысле эту роль уже закрывает `[[Finite Automaton]]`.
- Не стоит делать `UML State Machine Diagram` родителем для `State Machine`: это создаст ложную иерархию между концептом и нотацией.
- Не стоит преждевременно создавать отдельные заметки уровня `State`, `Event`, `Transition` и `Guard`, пока под них нет самостоятельного корпуса.
- Не стоит создавать специальные тематические template-файлы под эту тему: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`, развернутых в конкретные заметки.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── S/
    └── State Machine.md
```

## Что уже создано в Inbox

- `[[State Machine]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границу между engineering state machine и `[[Finite Automaton]]`
- [ ] Проверить связь между `[[State Machine]]` и `[[UML State Machine Diagram]]`
- [ ] Проверить, когда рядом нужны `Hierarchical State Machine` и `Statechart`
- [ ] Проверить `related`
