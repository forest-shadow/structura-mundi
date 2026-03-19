---
aliases:
  - Golang Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent:
status: draft
related:
  - "[[Go]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Testing]]"
tags: []
---

# Go Structure Proposal

## Краткое определение

Предлагаемая ветка для `Go` собирает базовые свойства языка, его стандартного инструментария и наиболее характерных моделей программирования.

## Выбранная оптика

- `area: computer-science`
- `domain: programming-languages`
- `section: go` (предлагаемое новое значение)

Почему так:

- `programming-languages` уже используется в базе как подходящий `domain` для языковых веток;
- `Go` естественно вписывается в него как отдельный тематический кластер;
- `section: go` полезен не для одной заметки, а для серии заметок о самом языке и его идиомах.

## Каноническое имя

- корневая обзорная заметка: `Go`
- `Golang` лучше хранить как `alias`, а не как отдельную каноническую заметку

## Рекомендуемая иерархия

```text
Go
├── Go Toolchain
├── Go Packages and Modules
├── Go Type System
├── Go Interfaces
├── Go Error Handling
├── Go Concurrency Model
│   ├── Go Goroutines
│   └── Go Channels
└── Go Testing
```

## Почему структура именно такая

- `Go` служит обзорной рамкой верхнего уровня.
- Большинство тем достаточно раскрывать как обычные `article`.
- Единственная оправданная дополнительная вложенность на текущем этапе — `Go Concurrency Model`, потому что `goroutines` и `channels` образуют плотную самостоятельную подветку.
- Уже существующую заметку `Testing Mind Model.md` лучше нормализовать до канонического узла `Go Testing`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── G/
    ├── Go.md
    ├── Go Toolchain.md
    ├── Go Packages and Modules.md
    ├── Go Type System.md
    ├── Go Interfaces.md
    ├── Go Error Handling.md
    ├── Go Concurrency Model.md
    ├── Go Goroutines.md
    ├── Go Channels.md
    └── Go Testing.md
```

## Что уже создано в Inbox

- `[[Go]]`
- `[[Go Toolchain]]`
- `[[Go Packages and Modules]]`
- `[[Go Type System]]`
- `[[Go Interfaces]]`
- `[[Go Error Handling]]`
- `[[Go Concurrency Model]]`
- `[[Go Goroutines]]`
- `[[Go Channels]]`
- `[[Go Testing]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, когда `Go Toolchain` стоит делить на `go build`, `go test`, `go mod`
- [ ] Решить, нужна ли отдельная заметка `Go Memory Model`
- [ ] Уточнить границы между `Go Interfaces` и `Go Type System`
- [ ] Подтвердить `section: go`
