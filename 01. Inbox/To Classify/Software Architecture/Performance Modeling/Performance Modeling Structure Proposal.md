---
aliases:
  - Performance Modeling Branch Structure Proposal
note_type: article
area: computer-science
domain: software-architecture
section: performance-modeling
parent:
status: draft
related:
  - "[[Software Architecture]]"
  - "[[Performance Modeling]]"
  - "[[Queuing Theory]]"
  - "[[Little's Law]]"
  - "[[Kendall Notation]]"
  - "[[Network Performance]]"
  - "[[Server]]"
  - "[[Server Process]]"
tags: []
---

# Performance Modeling Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную ветку заметок для формального разговора о нагрузке, очередях и пропускной способности системы внутри `Software Architecture`.

По правилам `Principia Rerum` `Queuing Theory` лучше не оставлять одиночной статьей без локального кластера: рядом естественно живут как минимум `Little's Law` и `Kendall Notation`.

## Выбранная оптика

- `Performance Modeling`
  - `area: computer-science`
  - `domain: software-architecture`
  - `section: performance-modeling`
  - `parent: [[Software Architecture]]`
- `Queuing Theory`
  - `area: computer-science`
  - `domain: software-architecture`
  - `section: performance-modeling`
  - `parent: [[Performance Modeling]]`
- `Little's Law`
  - `area: computer-science`
  - `domain: software-architecture`
  - `section: performance-modeling`
  - `parent: [[Performance Modeling]]`
- `Kendall Notation`
  - `area: computer-science`
  - `domain: software-architecture`
  - `section: performance-modeling`
  - `parent: [[Performance Modeling]]`

## Почему структура именно такая

- `Queuing Theory` в корпусе уже используется не только для сетей, но и для заметок `Server` и `Server Process`, поэтому слишком узко делать ее частью только `Network Performance`.
- `Performance Modeling` выступает здесь не как operational performance tuning, а как общий язык математического описания нагрузки, очередей, задержки, пропускной способности и коэффициента загрузки.
- `Little's Law` и `Kendall Notation` являются не случайными деталями внутри одной статьи, а повторно используемыми формальными аппаратами, которые стоит держать как отдельные статьи в одном кластере.
- `Network Performance` остается соседней прикладной веткой: она описывает сетевые метрики и поведение каналов, а не весь аппарат моделирования систем обслуживания.

## Рекомендуемая иерархия

```text
Software Architecture
└── Performance Modeling
    ├── Queuing Theory
    ├── Little's Law
    └── Kendall Notation
```

Поперечные связи:

```text
Queuing Theory ↔ Network Performance
Queuing Theory ↔ Server
Little's Law ↔ Server Process
Kendall Notation ↔ Server
```

## Что раскрывает каждая заметка

- `Performance Modeling`: обзорный узел для математических моделей поведения систем под нагрузкой.
- `Queuing Theory`: базовая рамка для описания очередей, поступления заявок, обслуживания и saturation.
- `Little's Law`: фундаментальная связь между concurrency, throughput и latency.
- `Kendall Notation`: компактный формальный язык для обозначения классов систем обслуживания вроде `M/M/1` и `M/M/c`.

## Что не стоит делать

- уводить `Queuing Theory` целиком в `networking`, будто это только сетевая тема;
- смешивать формальные модели нагрузки с чисто operational-практиками тюнинга в одной канонической заметке;
- создавать отдельные тематические template-файлы: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужен отдельный узел `Utilization`
- [ ] Проверить, когда рядом нужен отдельный узел `Queueing Delay`
- [ ] Проверить, когда модель `M/M/1` заслуживает самостоятельной статьи
- [ ] Проверить `related`
