---
aliases:
  - Performance Engineering Branch Structure Proposal
note_type: article
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Software Development]]"
status: seed
related:
  - "[[Software Development]]"
  - "[[Performance Engineering]]"
  - "[[Profiling]]"
  - "[[Performance Modeling]]"
  - "[[Go pprof]]"
tags: []
---

# Performance Engineering Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Performance Engineering` внутри `Software Development` по правилам `Principia Rerum`.

Для этой ветки предлагается рабочая рамка:

- `area: computer-science`
- `domain: software-development`
- `section: performance-engineering`

## Рекомендуемая иерархия

```text
Software Development
└── Performance Engineering
    └── Profiling
        ├── Profiling Targets and Signals
        ├── Profiling Workflow
        └── Profiling Overhead and Limits
```

## Почему структура именно такая

- `Performance Engineering` нужен как section-level overview, потому что `Profiling` не должен оставаться одиночной статьей без родительской инженерной рамки.
- `Profiling` оправдан как вложенный `overview`, потому что здесь быстро распадаются разные аспекты: измеряемые сигналы, способ чтения профиля и цена самого измерения.
- `[[Performance Modeling]]` не годится как родитель, потому что это соседняя теоретическая ветка про модели нагрузки, а не developer workflow.
- `[[Go pprof]]` не годится как корень, потому что это language-specific инструмент внутри более широкой практики profiling.

## Что не стоит делать прямо сейчас

- создавать отдельный `section: profiling`, потому что нужен не один термин, а устойчивый раздел про performance-oriented tooling;
- смешивать profiling с distributed observability в одной корневой заметке;
- создавать отдельные тематические template-файлы: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Созданные seed-заготовки

- `[[Performance Engineering]]`
- `[[Profiling]]`
- `[[Profiling Targets and Signals]]`
- `[[Profiling Workflow]]`
- `[[Profiling Overhead and Limits]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Benchmarking` и `Performance Regression Analysis`
- [ ] Уточнить границу между profiling и tracing
- [ ] Проверить `related`
