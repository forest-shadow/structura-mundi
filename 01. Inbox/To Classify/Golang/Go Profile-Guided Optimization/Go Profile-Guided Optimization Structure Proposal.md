---
aliases:
  - Go PGO Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Toolchain]]"
status: seed
related:
  - "[[Go Toolchain]]"
  - "[[Go Profile-Guided Optimization]]"
  - "[[Profile-Guided Optimization]]"
tags: []
---

# Go Profile-Guided Optimization Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Go Profile-Guided Optimization` как language-specific случая для общего concept `[[Profile-Guided Optimization]]`.

## Рекомендуемая иерархия

```text
Go
└── Go Toolchain
    └── Go Profile-Guided Optimization
        ├── Go pprof for PGO
        ├── Go PGO Workflow
        └── Go PGO Constraints and Trade-offs
```

## Почему структура именно такая

- Ветка нужна как Go-specific implementation case, а не как замена общего concept `[[Profile-Guided Optimization]]`.
- `Go pprof for PGO` выражает конкретную роль уже существующего `[[Go pprof]]` в Go-oriented PGO workflow.
- Отдельный второй overview `Go pprof` внутри этой ветки не нужен.

## Что не стоит делать прямо сейчас

- дублировать общий PGO concept внутри Go-ветки;
- создавать новый `section: pgo`;
- создавать специальные template-файлы под PGO.

## Созданные seed-заготовки

- `[[Go Profile-Guided Optimization]]`
- `[[Go pprof for PGO]]`
- `[[Go PGO Workflow]]`
- `[[Go PGO Constraints and Trade-offs]]`
