---
aliases:
  - Докер Structure Proposal
  - Структура ветки Docker
note_type: article
area: computer-science
domain: operating-systems
section: containerization
parent: "[[Containerization]]"
status: draft
related:
  - "[[Computer Science]]"
  - "[[Operating Systems]]"
  - "[[Containerization]]"
  - "[[Docker]]"
tags: []
---

# Docker Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Docker`, в которую естественно помещается рассмотрение этого понятия по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: operating-systems`
- `section: containerization` (предлагаемое новое значение)

Почему так:

- `Docker` не стоит помещать напрямую в `distributed-systems`, потому что контейнеризация может использоваться и вне распределённой оркестрации;
- не стоит делать главной оптикой и `software-architecture`, потому что в основе темы лежат механизмы изоляции процессов, исполнения и упаковки поверх ядра ОС;
- `operating-systems` лучше задаёт главную рамку для контейнеров, потому что именно здесь естественно объяснять связь с `namespaces`, `cgroups`, process isolation и runtime boundary;
- `Containerization` оправдана как section-level overview, потому что `Docker` — это не весь домен ОС и не вся теория контейнеров, а один конкретный узел внутри более широкого кластера.

## Канонические имена

- area-level root: `Computer Science`
- domain-root overview: `Operating Systems`
- section-level overview: `Containerization`
- article: `Docker`

Русская форма `Докер` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Computer Science
└── Operating Systems
    └── Containerization
        └── Docker
```

## Почему структура именно такая

- `Operating Systems` лучше делать domain-root overview, потому что контейнеризация опирается на системные механизмы ядра и execution model.
- `Containerization` лучше сделать section-level overview, потому что рядом с `Docker` естественно ожидаются другие заметки: `Container Image`, `Container Runtime`, `Linux Namespaces`, `cgroups`, OCI и container networking.
- `Docker` должен быть обычной `article`, а не обзорной заметкой, потому что речь идёт об одном конкретном инструментальном и экосистемном узле.
- Такая структура сохраняет принцип минимальной глубины: добавляется только один локальный overview, который действительно нужен для роста ветки.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Docker` напрямую под `Computer Science` или напрямую под `Operating Systems`, если ожидается рост контейнерной ветки.
- Не стоит подчинять `Docker` ветке `Distributed Systems` только потому, что он часто используется рядом с Kubernetes.
- Не стоит сразу создавать отдельные заметки `Container Runtime`, `OCI`, `Docker Compose` и `Kubernetes`, если рядом ещё нет устойчивого корпуса.
- Не стоит создавать отдельные тематические template-файлы под эту ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── C/
│   ├── Computer Science.md
│   └── Containerization.md
├── D/
│   └── Docker.md
└── O/
    └── Operating Systems.md
```

## Что уже создано в Inbox

- `[[Computer Science]]`
- `[[Operating Systems]]`
- `[[Containerization]]`
- `[[Docker]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Docker` нужны `Container Image` и `Container Runtime`
- [ ] Подтвердить `section: containerization`
- [ ] Проверить `related`
