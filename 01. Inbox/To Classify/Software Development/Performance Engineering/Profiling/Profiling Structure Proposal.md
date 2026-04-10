---
aliases:
  - Profiling Branch Structure Proposal
note_type: article
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Performance Engineering]]"
status: seed
related:
  - "[[Profiling]]"
  - "[[Performance Engineering]]"
  - "[[Go pprof]]"
  - "[[Performance Modeling]]"
tags: []
---

# Profiling Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Profiling` внутри `Performance Engineering` по правилам `Principia Rerum`.

## Рекомендуемая иерархия

```text
Performance Engineering
└── Profiling
    ├── Profiling Targets and Signals
    ├── Profiling Workflow
    └── Profiling Overhead and Limits
```

## Почему структура именно такая

- `Profiling` здесь оправдан как `overview`, потому что это не один прием и не одна утилита, а целый класс практик анализа исполнения.
- `Profiling Targets and Signals` отделяет типы измерений от конкретных инструментов.
- `Profiling Workflow` отделяет reading practice и decision loop от описания самих профилей.
- `Profiling Overhead and Limits` нужен отдельно, чтобы ограничения метода не растворялись в общей статье.

## Что не стоит делать прямо сейчас

- сводить весь profiling к одному language-specific инструменту вроде `pprof`;
- смешивать profiling и benchmarking в одной заметке, будто это один и тот же метод;
- создавать тематические template-файлы под performance notes.

## Созданные seed-заготовки

- `[[Profiling]]`
- `[[Profiling Targets and Signals]]`
- `[[Profiling Workflow]]`
- `[[Profiling Overhead and Limits]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужны отдельные notes про sampling profiler и instrumentation profiler
- [ ] Проверить, когда рядом нужен `Benchmarking`
- [ ] Проверить `related`
