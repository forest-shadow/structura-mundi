---
aliases:
  - Golang Toolchain
  - Инструментарий Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Commands]]"
  - "[[Go Packages and Modules]]"
  - "[[Go Escape Analysis]]"
  - "[[Go Testing]]"
  - "[[Go Runtime Diagnostics]]"
  - "[[Go pprof]]"
tags: []
---

# Go Toolchain

## Краткое определение области

`Go Toolchain` - это обзорная ветка про стандартный инструментарий Go для сборки, запуска, тестирования, форматирования, управления модулями и доступа к низкоуровневым служебным инструментам.

## Что входит в эту тему

- `[[Go Commands]]`
- `[[Go Packages and Modules]]`
- `[[Go Testing]]`
- `[[Go Runtime Diagnostics]]`

## Как устроена ветка

- `Go Commands` собирает базовые CLI-команды вроде `go build`, `go run`, `go test`, `go fmt` и `go mod`.
- `Go Packages and Modules` остается отдельной статьей, потому что она описывает модель пакетов, модулей и зависимостей, а не только интерфейс командной строки.
- `Go Testing` остается отдельной статьей, потому что `go test` — лишь вход в более широкую тему testing model в Go.
- `Go Runtime Diagnostics` собирает диагностические инструменты и workflows, часть которых вызывается через `go tool`, но смысл ветки шире простого списка команд.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Commands]]`, чтобы увидеть базовую карту стандартного CLI.
2. Затем перейти к `[[go build]]`, `[[go run]]` и `[[go test]]`, если нужен повседневный цикл разработки.
3. После этого читать `[[go mod]]` вместе с `[[Go Packages and Modules]]`.
4. Для диагностики и profiling перейти к `[[Go Runtime Diagnostics]]` и `[[Go pprof]]`.

## Соседние overview-ветки

- `[[Go]]`
- `[[Go Runtime Diagnostics]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужен отдельный узел `Go Build Artifacts`
- [ ] Проверить, когда `go tool` должен стать самостоятельной заметкой
- [ ] Уточнить границу между `Go Commands`, `Go Packages and Modules` и `Go Runtime Diagnostics`
- [ ] Проверить `related`
