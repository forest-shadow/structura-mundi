---
aliases:
  - Golang Commands
  - Go CLI Commands
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Toolchain]]"
status: seed
related:
  - "[[Go Toolchain]]"
  - "[[Go Packages and Modules]]"
  - "[[Go Testing]]"
  - "[[Go Runtime Diagnostics]]"
tags: []
---

# Go Commands

## Краткое определение области

`Go Commands` - это обзорная ветка про основные команды CLI `go`, через которые обычно происходит повседневная работа с Go-проектом: сборка, запуск, тестирование, форматирование и управление модулями.

## Что входит в эту тему

- `[[go build]]`
- `[[go run]]`
- `[[go test]]`
- `[[go fmt]]`
- `[[go mod]]`

## Как устроена ветка

- `go build` отвечает за сборку пакетов и исполняемых файлов.
- `go run` нужен для быстрого запуска программы без отдельного ручного шага исполнения бинарника.
- `go test` является входом в testing workflow, но сама модель тестирования раскрывается шире в `[[Go Testing]]`.
- `go fmt` выражает встроенную норму форматирования в экосистеме Go.
- `go mod` управляет модульной структурой и зависимостями, но опирается на более общую тему `[[Go Packages and Modules]]`.

## Рекомендуемый маршрут чтения

1. Начать с `[[go build]]` и `[[go run]]`, чтобы понять базовый цикл сборки и запуска.
2. Затем перейти к `[[go test]]` и сопоставить его с `[[Go Testing]]`.
3. После этого читать `[[go fmt]]` как часть idiomatic workflow.
4. Завершить `[[go mod]]`, если нужен dependency и module context.

## Соседние overview-ветки

- `[[Go Toolchain]]`
- `[[Go Runtime Diagnostics]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда в ветке понадобятся `go install`, `go generate` и `go tool`
- [ ] Проверить, нужен ли рядом отдельный article про command flags и package patterns
- [ ] Проверить `related`
