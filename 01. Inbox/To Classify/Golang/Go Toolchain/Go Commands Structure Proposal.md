---
aliases:
  - Go Commands Knowledge Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Toolchain]]"
status: seed
related:
  - "[[Go Toolchain]]"
  - "[[Go Commands]]"
  - "[[Go Packages and Modules]]"
  - "[[Go Testing]]"
  - "[[Go Runtime Diagnostics]]"
tags: []
---

# Go Commands Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Go Commands`, в которую естественно помещается рассмотрение такого понятия, как `Go commands`, по правилам `Principia Rerum`.

Для этой ветки используется уже подтвержденная таксономия:

- `area: computer-science`
- `domain: programming-languages`
- `section: go`

## Рекомендуемая иерархия

```text
Programming Languages
└── Go
    └── Go Toolchain
        └── Go Commands
            ├── go build
            ├── go run
            ├── go test
            ├── go fmt
            └── go mod
```

## Почему структура именно такая

- `Go Toolchain` оправдан как вложенный `overview`, потому что тема стандартного инструментария Go шире списка команд и включает связи с testing, modules и diagnostics.
- `Go Commands` нужен как отдельный `sub-overview`, потому что команда `go` задает устойчивую ось чтения внутри toolchain: пользователь чаще думает не только о toolchain вообще, а о конкретных повседневных командах.
- `go build`, `go run`, `go test`, `go fmt` и `go mod` лучше начинать как отдельные `article`, потому что каждая из этих команд уже является самостоятельной канонической точкой входа.
- `go test` не должен поглощать всю тему testing: по `Principia Rerum` командный интерфейс и более широкая модель тестирования лучше держать как соседние, а не тождественные узлы.
- `go mod` нужно держать рядом с командами, но не превращать ветку команд в замену статьи `[[Go Packages and Modules]]`, потому что команды и модель модулей не совпадают по границам.

## Что не стоит создавать заранее

- отдельный `section: go-commands`, потому что `section: go` уже достаточно, а локальная вложенность выражается через `parent`;
- отдельные тематические template-файлы под Go toolchain или Go commands, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`;
- слишком раннее дробление на заметки про каждый флаг и каждую подкоманду `go mod`, пока для этого нет плотного корпуса;
- отдельную заметку `Go CLI`, если она будет просто дублировать `Go Commands`.

## Созданные seed-заготовки

- `[[Go Commands]]`
- `[[go build]]`
- `[[go run]]`
- `[[go test]]`
- `[[go fmt]]`
- `[[go mod]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `go install`, `go generate` и `go tool`
- [ ] Проверить, когда `go mod tidy`, `go mod download` и `go mod vendor` заслуживают отдельных статей
- [ ] Проверить `related`
