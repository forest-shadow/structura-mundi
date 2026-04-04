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
tags: []
---

# Computer Science Structure Proposal

## Краткое определение

Предлагаемая ветка для `Computer Science` собирает под одним корневым обзорным узлом основные доменные ветки всей области: `algorithms`, `programming-languages`, `computer-architecture`, `databases`, `distributed-systems`, `networking`, `frontend-engineering`, `software-architecture` и `operating-systems`.

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
└── Operating Systems
    ├── Processes and Threads
    ├── System Calls
    ├── File Systems
    ├── Virtual Memory
    └── Containerization
        └── Docker
```

## Почему структура именно такая

- `Computer Science` нужен как root `overview`, потому что здесь уже есть несколько устойчивых доменных веток, а не одна локальная тема.
- Дочерние узлы верхнего уровня лучше делать domain-overview notes, а не сразу вести от `Computer Science` к случайным специализированным заметкам.
- `Operating Systems` теперь включает не только execution и memory-management, но и контейнерную ветку `Containerization`, в которую естественно помещается `Docker`.
- `Docker` не стоит поднимать на уровень domain-root рядом с `Operating Systems`, потому что это уже product/ecosystem-level термин внутри более узкой системной ветки.

## Что не стоит создавать заранее

- отдельные overview-слои только ради симметрии между всеми возможными subfields;
- заметки вроде `Theory`, `Systems`, `Applications`, если за ними пока нет устойчивых корпусов;
- избыточные промежуточные узлы между `Computer Science` и domain-overview notes.

## Что создано в Inbox

- `[[Computer Science]]`
- `[[Operating Systems]]`
- `[[Containerization]]`
- `[[Docker]]`

## Что стоит раскрыть дальше

- [ ] Проверить, что `Computer Science` остается area-level root без `domain` и `section`
- [ ] Проверить, когда в OS-ветке рядом с `Docker` нужны другие containerization notes
- [ ] Проверить, какие существующие корни еще стоит переподвесить под domain-overview nodes
