---
aliases:
  - Observability Structure Proposal
note_type: article
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Service Reliability]]"
status: draft
related:
  - "[[Observability]]"
  - "[[Monitoring]]"
  - "[[Telemetry]]"
  - "[[Dashboard]]"
  - "[[Synthetic Monitoring]]"
  - "[[White-box and Black-box Monitoring]]"
tags:
  - observability
  - reliability
---

# Observability Structure Proposal

## Краткое определение

Предлагаемое устройство подветки `Observability` внутри `Service Reliability` в домене `Distributed Systems`.

## Рекомендуемая иерархия

```text
Service Reliability
├── Telemetry
│   ├── Metrics
│   ├── Logging
│   └── Distributed Tracing
└── Observability
    └── Monitoring
        ├── Dashboard
        ├── Synthetic Monitoring
        └── White-box and Black-box Monitoring
```

Переиспользуемые соседние заметки:

- `Telemetry`
- `Metrics`
- `Logging`
- `Distributed Tracing`
- `Alerting and Monitoring Practices`

## Почему структура именно такая

- `Observability` лучше оформлять как отдельный `overview`, потому что это не одиночный термин, а устойчивый кластер заметок про вывод внутреннего состояния системы по внешним сигналам.
- `Observability` не стоит смешивать с `Telemetry` в одной заметке: телеметрия описывает сами сигналы и данные, а observability описывает инженерное свойство и практику работы с ними.
- `Observability` не стоит оформлять как склеенный узел `Observability and Monitoring`, потому что по правилам `Principia Rerum` одна каноническая заметка должна по возможности соответствовать одному устойчивому объекту знания.
- `Monitoring` уместен как дочерний `overview`, а не как sibling для `Telemetry`: monitoring является прикладной operational-практикой внутри observability-ветки, а не отдельным родовым классом сигналов.
- `Dashboard`, `Synthetic Monitoring` и `White-box and Black-box Monitoring` естественно подчинять именно `Monitoring`, потому что это разные способы организации и чтения наблюдения, а не отдельные виды телеметрии.
- `Metrics`, `Logging` и `Distributed Tracing` не нужно переносить под `Observability`: они уже образуют осмысленную соседнюю ветку внутри `Telemetry` и должны связываться с observability через `related`, а не через дублирующую иерархию.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельную каноническую заметку `Observability and Monitoring`, если та же логика чище выражается через узлы `Observability` и `Monitoring`.
- Не стоит подчинять `Metrics`, `Logging` и `Distributed Tracing` заметке `Observability`, если они уже живут как виды телеметрии.
- Не стоит вводить новый `domain` или новый `section`: текущих `domain: distributed-systems` и `section: service-reliability` достаточно.
- Не стоит делать специальные templates для observability-ветки вне стандартных `Article Template` и `Overview Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный article про `Instrumentation`
- [ ] Проверить, когда рядом нужны `Service Level Indicator` и `Alerting`
- [ ] Проверить границу между `Monitoring` и `Alerting and Monitoring Practices`
- [ ] Проверить `related`
