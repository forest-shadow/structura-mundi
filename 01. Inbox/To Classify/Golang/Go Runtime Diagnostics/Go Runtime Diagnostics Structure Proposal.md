---
aliases:
  - Go Diagnostics Structure Proposal
  - Runtime Diagnostics in Go Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Runtime Diagnostics]]"
  - "[[Go pprof]]"
  - "[[Go Toolchain]]"
  - "[[Go Memory Management]]"
  - "[[Observability in Go Servers]]"
tags: []
---

# Go Runtime Diagnostics Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Go Runtime Diagnostics`, в которую естественно помещается рассмотрение `Go pprof` по правилам `Principia Rerum`.

Для этой ветки используется уже подтвержденная таксономия:

- `area: computer-science`
- `domain: programming-languages`
- `section: go`

## Рекомендуемая иерархия

```text
Programming Languages
└── Go
    └── Go Runtime Diagnostics
        └── Go pprof
            ├── Go pprof Profile Types
            ├── Go pprof Collection Methods
            └── Go pprof Analysis Workflow
```

## Почему структура именно такая

- `Go Runtime Diagnostics` нужен как вложенный `overview`, потому что pprof относится не только к toolchain и не только к server observability, а к runtime-диагностике Go-программ.
- `Go pprof` оформляется как `overview`, потому что термин объединяет пакеты `runtime/pprof` и `net/http/pprof`, команду `go tool pprof`, profile data и workflow анализа.
- `Go pprof Profile Types` нужен для CPU, heap, goroutine, block и mutex профилей.
- `Go pprof Collection Methods` нужен для способов получения профилей: programmatic collection, HTTP endpoints, benchmark flags и production-gated endpoints.
- `Go pprof Analysis Workflow` нужен для чтения профилей через `go tool pprof`, сравнения профилей и поиска bottleneck-ов.

## Что не стоит создавать заранее

- отдельный `section: pprof`, потому что `section: go` уже достаточен, а логическая вложенность выражается через `parent`;
- отдельную заметку `pprof` без Go-уточнения, пока фокус задан именно как pprof в контексте Go;
- отдельный template-файл под Go diagnostics или pprof: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`;
- отдельные статьи по каждому profile type до появления достаточного корпуса, если их можно раскрыть внутри `Go pprof Profile Types`.

## Созданные seed-заготовки

- `[[Go Runtime Diagnostics]]`
- `[[Go pprof]]`
- `[[Go pprof Profile Types]]`
- `[[Go pprof Collection Methods]]`
- `[[Go pprof Analysis Workflow]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда `Go Execution Tracer` должен стать соседним узлом
- [ ] Решить, когда нужны отдельные articles для CPU, heap, goroutine, block и mutex профилей
- [ ] Проверить `related`
