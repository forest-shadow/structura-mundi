---
aliases:
  - Packages and Modules in Go
  - Пакеты и модули Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go]]"
status: seed
related:
  - "[[Go]]"
  - "[[Go Toolchain]]"
  - "[[Go Type System]]"
  - "[[go mod]]"
tags: []
---

# Go Packages and Modules

## Краткое определение области

`Go Packages and Modules` - это обзорная ветка про то, как в Go устроены единицы организации кода, импорта и версионирования: package как локальная единица namespace и compilation, module как единица dependency management и versioned distribution.

## Что входит в эту тему

- `[[Go Packages]]`
- `[[Go Modules]]`
- `[[Go Import Paths]]`
- `[[go.mod]]`

## Как устроена ветка

- `Go Packages` описывает локальную организацию кода, package clause, экспортируемые идентификаторы и границы компиляции.
- `Go Modules` описывает верхний уровень module graph, versioning и dependency boundaries.
- `Go Import Paths` связывает package model с тем, как код адресуется и импортируется.
- `go.mod` остается отдельной статьей о самом файле и его роли, хотя командный интерфейс работы с ним раскрывается рядом через `[[go mod]]`.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Packages]]`, чтобы увидеть базовую единицу организации кода.
2. Затем перейти к `[[Go Import Paths]]`, чтобы понять, как packages адресуются снаружи.
3. После этого читать `[[Go Modules]]` как более внешний слой dependency и versioning model.
4. Завершить `[[go.mod]]` и сопоставить его с `[[go mod]]`, если нужен operational workflow.

## Соседние overview-ветки

- `[[Go]]`
- `[[Go Toolchain]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Go Package Initialization` и `Go Workspaces`
- [ ] Уточнить границу между `Go Modules` и `go mod`
- [ ] Проверить `related`
