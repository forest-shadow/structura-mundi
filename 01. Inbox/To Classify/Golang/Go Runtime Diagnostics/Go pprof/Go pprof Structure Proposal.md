---
aliases:
  - pprof Structure Proposal
  - Go pprof Branch Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Runtime Diagnostics]]"
status: seed
related:
  - "[[Go pprof]]"
  - "[[Go Runtime Diagnostics]]"
  - "[[Go Toolchain]]"
  - "[[Observability in Go Servers]]"
tags: []
---

# Go pprof Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Go pprof` по правилам `Principia Rerum`.

## Рекомендуемая иерархия

```text
Go Runtime Diagnostics
└── Go pprof
    ├── Go pprof Profile Types
    ├── Go pprof Collection Methods
    └── Go pprof Analysis Workflow
```

## Почему структура именно такая

- Каноническое имя `Go pprof` сохраняет Go-контекст и не смешивает заметку с более широким pprof-форматом вне Go.
- `pprof`, `go tool pprof`, `runtime/pprof` и `net/http/pprof` уходят в `aliases`, потому что это связанные формы обращения к тому же Go-ориентированному узлу.
- Корневая заметка `Go pprof` является `overview`, потому что pprof включает profile types, collection methods и analysis workflow.
- Дочерние статьи разделяют вопрос "что измеряется", вопрос "как профиль получить" и вопрос "как профиль читать".

## Что не стоит делать прямо сейчас

- создавать отдельную заметку `pprof` без Go-уточнения;
- создавать отдельный `section: pprof`;
- дробить CPU, heap, goroutine, block и mutex profiles на отдельные articles до появления плотного корпуса;
- создавать тематические template-файлы под Go diagnostics.

## Созданные seed-заготовки

- `[[Go pprof]]`
- `[[Go pprof Profile Types]]`
- `[[Go pprof Collection Methods]]`
- `[[Go pprof Analysis Workflow]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, где проходит граница между pprof и `go tool trace`
- [ ] Уточнить production security для `net/http/pprof`
- [ ] Проверить `related`
