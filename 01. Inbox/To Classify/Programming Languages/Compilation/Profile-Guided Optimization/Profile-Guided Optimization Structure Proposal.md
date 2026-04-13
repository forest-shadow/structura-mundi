---
aliases:
  - PGO Structure Proposal
  - Profile Guided Optimization Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Compilation]]"
  - "[[Profile-Guided Optimization]]"
  - "[[Go Profile-Guided Optimization]]"
tags: []
---

# Profile-Guided Optimization Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Profile-Guided Optimization`, в которую можно поместить рассмотрение PGO по правилам `Principia Rerum`.

Для этой ветки используется уже подтвержденная таксономия:

- `area: computer-science`
- `domain: programming-languages`
- `section: compilation`

## Рекомендуемая иерархия

```text
Programming Languages
└── Compilation
    └── Profile-Guided Optimization
        ├── Profile-Guided Optimization Profile Collection
        ├── Profile-Guided Optimization Feedback Loop
        └── Profile-Guided Optimization Constraints and Trade-offs
```

## Почему структура именно такая

- `Profile-Guided Optimization` нужен как вложенный `overview`, потому что PGO является устойчивым cross-language compilation concept, а не языково-специфичным частным термином.
- Каноническое имя берёт полную форму `Profile-Guided Optimization`, а `PGO` уходит в `aliases`, потому что полное имя менее двусмысленно в общем корпусе.
- Дочерние статьи разделяют происхождение профильных данных, сам optimization loop и ограничения подхода.
- `Go Profile-Guided Optimization` должен связываться с этой веткой как language-specific implementation case, а не подменять собой общий concept.

## Что не стоит создавать заранее

- отдельный `section: pgo`, потому что `section: compilation` уже задаёт нужный локальный кластер;
- отдельную заметку `PGO in Go` как общий concept всей ветки;
- тематические template-файлы под compilation optimizations: по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`;
- слишком раннее дробление на vendor- и compiler-specific ветки, если пока достаточно общего compilation concept и одного language-specific случая.

## Созданные seed-заготовки

- `[[Profile-Guided Optimization]]`
- `[[Profile-Guided Optimization Profile Collection]]`
- `[[Profile-Guided Optimization Feedback Loop]]`
- `[[Profile-Guided Optimization Constraints and Trade-offs]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны notes про instrumentation-based и sampling-based PGO
- [ ] Решить, когда рядом нужен узел про link-time optimization
- [ ] Проверить `related`
