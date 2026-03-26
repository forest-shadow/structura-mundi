---
aliases:
  - CS Structure Proposal
note_type: article
area: computer-science
domain:
section:
parent:
status: draft
related:
  - "[[Computer Science]]"
  - "[[Algorithms]]"
  - "[[Programming Languages]]"
  - "[[Networking]]"
  - "[[Operating Systems]]"
tags: []
---

# Computer Science Structure Proposal

## Краткое определение

Предлагаемая ветка для `Computer Science` собирает под одним корневым обзорным узлом основные доменные ветки всей области: `algorithms`, `programming-languages`, `databases`, `distributed-systems`, `networking`, `frontend-engineering`, `system-design` и `operating-systems`.

## Выбранная оптика

- `area: computer-science`
- `domain:` пусто для `area-level root overview`
- `section:` пусто для `area-level root overview`

Почему так:

- `Computer Science` находится выше конкретных `domain`, поэтому существующие доменные значения не подходят для корневого area-level overview;
- обновленная модель `Principia Rerum` явно разрешает для area-level root пустые `domain` и `section`;
- это позволяет не вводить искусственные служебные значения ради одной корневой заметки;
- дочерние domain-overview notes при этом остаются внутри своих нормальных `domain`.

## Каноническое имя

- корневая обзорная заметка: `Computer Science`
- `CS` и `Computer Science Field` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Computer Science
├── Algorithms
│   ├── Automata Theory
│   └── Algorithm Analysis
├── Programming Languages
│   ├── Go
│   └── JavaScript
├── Databases
│   ├── Database Transactions
│   ├── ACID
│   └── Transaction Isolation Levels
├── Distributed Systems
│   ├── Distributed Systems Problems
│   │   └── Dual Write
│   ├── Caching
│   ├── Event-Driven Architecture
│   └── Telemetry
├── Networking
│   ├── Internet
│   │   ├── TCP IP Model
│   │   ├── IP Addressing
│   │   ├── DNS
│   │   └── Routing
│   └── OSI Model
├── Frontend Engineering
│   ├── React
│   ├── CSS
│   ├── Browser Page Processing
│   ├── Browser Rendering
│   └── CORS
├── System Design
│   ├── Design Principles
│   │   └── SOLID
│   ├── Dependency Management
│   ├── Clean Architecture
│   └── Service Reliability
└── Operating Systems
    ├── Processes and Threads
    ├── System Calls
    ├── File Systems
    └── Virtual Memory
```

## Почему структура именно такая

- `Computer Science` нужен как root `overview`, потому что здесь уже есть несколько устойчивых доменных веток, а не одна локальная тема.
- Дочерние узлы верхнего уровня лучше делать domain-overview notes, а не сразу вести от `Computer Science` к случайным специализированным заметкам.
- `Algorithms`, `Programming Languages`, `Distributed Systems`, `Networking`, `Frontend Engineering` и `Operating Systems` уже имеют достаточно плотные или ожидаемо плотные подветки.
- Внутри `Distributed Systems` уже стоит отражать, что `Dual Write` живет под `Distributed Systems Problems`, а `Event-Driven Architecture` выступает как отдельная подветка.
- `Databases` пока тоньше, но все равно оправдан как доменная рамка, потому что без него корневая ветка начинает смешивать уровни абстракции.
- `System Design` уже перестает быть только thin-wrapper вокруг `Service Reliability`, потому что внутри него оформляются ветки `Design Principles`, `Dependency Management` и `Clean Architecture`.

## Что не стоит создавать заранее

- отдельные overview-слои только ради симметрии между всеми возможными subfields;
- заметки вроде `Theory`, `Systems`, `Applications`, если за ними пока нет устойчивых корпусов;
- избыточные промежуточные узлы между `Computer Science` и domain-overview notes.

## Что создано в Inbox

- `[[Computer Science]]`
- `[[Algorithms]]`
- `[[Programming Languages]]`
- `[[Databases]]`
- `[[Distributed Systems]]`
- `[[Networking]]`
- `[[Frontend Engineering]]`
- `[[System Design]]`

## Что стоит раскрыть дальше

- [ ] Проверить, что `Computer Science` остается area-level root без `domain` и `section`
- [ ] Проверить, что domain-root overview notes под ней остаются без `section`
- [ ] Проверить, какие существующие корни еще стоит переподвесить под domain-overview nodes
