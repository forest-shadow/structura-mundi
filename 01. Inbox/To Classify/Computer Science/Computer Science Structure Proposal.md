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
  - "[[Computer Architecture]]"
  - "[[Networking]]"
  - "[[Operating Systems]]"
  - "[[Software Development]]"
tags: []
---

# Computer Science Structure Proposal

## Краткое определение

Предлагаемая ветка для `Computer Science` собирает под одним корневым обзорным узлом основные доменные ветки всей области: `algorithms`, `programming-languages`, `computer-architecture`, `databases`, `distributed-systems`, `networking`, `frontend-engineering`, `software-architecture`, `operating-systems` и `software-development`.

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
├── Computer Architecture
│   └── Instruction Set Architecture
├── Databases
│   ├── Database Transactions
│   ├── ACID
│   └── Transaction Isolation Levels
├── Distributed Systems
│   ├── Distributed Systems Problems
│   │   └── Dual Write
│   ├── Caching
│   ├── Event-Driven Architecture
│   └── Service Reliability
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
├── Software Architecture
│   ├── Design Principles
│   │   └── SOLID
│   ├── Dependency Management
│   └── Clean Architecture
├── Operating Systems
│   ├── Processes and Threads
│   ├── System Calls
│   ├── File Systems
│   ├── Virtual Memory
│   └── Containerization
│       └── Docker
└── Software Development
    └── Vim
        ├── Vim Modes
        ├── Vim Motions
        ├── Vim Operators
        ├── Vim Text Objects
        ├── Vim Registers
        ├── Vim Macros
        └── Vim Buffers, Windows, and Tabs
```

## Почему структура именно такая

- `Computer Science` нужен как root `overview`, потому что здесь уже есть несколько устойчивых доменных веток, а не одна локальная тема.
- Дочерние узлы верхнего уровня лучше делать domain-overview notes, а не сразу вести от `Computer Science` к случайным специализированным заметкам.
- `Software Development` оправдан как отдельный domain-root, потому что заметки про редакторы, version control, build tooling и другие инструменты разработки не сводятся ни к `Programming Languages`, ни к `Software Architecture`.
- `Vim` не стоит подвешивать напрямую под `Programming Languages`, потому что это не language-specific механизм, а самостоятельный инструментальный кластер.

## Что не стоит создавать заранее

- отдельные overview-слои только ради симметрии между всеми возможными subfields;
- заметки вроде `Theory`, `Systems`, `Applications`, если за ними пока нет устойчивых корпусов;
- избыточные промежуточные узлы между `Computer Science` и domain-overview notes.

## Что стоит раскрыть дальше

- [ ] Проверить, что `Computer Science` остается area-level root без `domain` и `section`
- [ ] Проверить, когда в `Software Development` рядом с `Vim` нужны `Git`, build tooling и testing tooling
- [ ] Проверить, какие существующие корни еще стоит переподвесить под domain-overview nodes
