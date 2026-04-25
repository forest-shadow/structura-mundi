---
aliases:
  - Go Packages and Modules Knowledge Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Packages and Modules]]"
  - "[[Go Toolchain]]"
  - "[[go mod]]"
tags: []
---

# Go Packages and Modules Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Go Packages and Modules`, в которую естественно помещается рассмотрение такого понятия, как `Go Packages and Modules`, по правилам `Principia Rerum`.

Для этой ветки используется уже подтвержденная таксономия:

- `area: computer-science`
- `domain: programming-languages`
- `section: go`

## Рекомендуемая иерархия

```text
Programming Languages
└── Go
    └── Go Packages and Modules
        ├── Go Packages
        ├── Go Import Paths
        ├── Go Modules
        └── go.mod
```

## Почему структура именно такая

- `Go Packages and Modules` оправдан как вложенный `overview`, потому что тема уже не сводится к одной статье: она объединяет несколько устойчивых осей чтения про package boundaries, import addressing и module-level dependency model.
- `Go Packages` нужен как отдельная статья, потому что package в Go является самостоятельной канонической единицей понимания языка.
- `Go Modules` нужен как отдельная статья, потому что module в Go не совпадает по смыслу с package и живет на другом уровне абстракции.
- `Go Import Paths` лучше держать отдельной статьей, потому что это связующее понятие между physical layout, package identity и import mechanics.
- `go.mod` стоит держать внутри этой ветки как отдельную статью о самом файле и его declarative роли, но не путать ее с командным интерфейсом `[[go mod]]`, который живет в `[[Go Commands]]`.

## Что не стоит создавать заранее

- отдельный `section: go-packages`, потому что `section: go` уже достаточен, а локальная вложенность должна выражаться через `parent`;
- отдельные тематические template-файлы под packages/modules notes, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`;
- преждевременное дробление на отдельные статьи про каждую директиву `go.mod`, пока нет плотного корпуса;
- попытку сделать `Go Packages and Modules` дочерней веткой `Go Toolchain`, потому что package/module model шире operational CLI workflow.

## Созданные seed-заготовки

- `[[Go Packages and Modules]]`
- `[[Go Packages]]`
- `[[Go Import Paths]]`
- `[[Go Modules]]`
- `[[go.mod]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужен `Go Workspaces`
- [ ] Проверить, когда `replace`, `require` и `module path` заслуживают отдельных статей
- [ ] Проверить `related`
