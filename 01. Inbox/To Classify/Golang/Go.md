---
aliases:
  - Golang
  - Go Language
  - Язык Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent:
status: seed
related:
  - "[[Go Toolchain]]"
  - "[[Go Packages and Modules]]"
  - "[[Go Type System]]"
  - "[[Go Interfaces]]"
  - "[[Go Error Handling]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Testing]]"
tags: []
---

# Go

## Краткое определение области

Обзорная заметка для языка Go как самостоятельной ветки знаний: языка, его стандартного инструментария, модели типов, работы с ошибками и характерных concurrency-механизмов.

## Что входит в эту тему

- `[[Go Toolchain]]`
- `[[Go Packages and Modules]]`
- `[[Go Type System]]`
- `[[Go Interfaces]]`
- `[[Go Error Handling]]`
- `[[Go Concurrency Model]]`
- `[[Go Testing]]`

## Как устроена ветка

- `Go` служит обзорным узлом верхнего уровня.
- Большинство тем раскрываются как обычные `article`.
- Единственный оправданный `sub-overview` на текущем этапе — `[[Go Concurrency Model]]`, потому что внутри него естественно живут `[[Go Goroutines]]` и `[[Go Channels]]`.

## Рекомендуемый маршрут чтения

1. Начать с `[[Go Toolchain]]` и `[[Go Packages and Modules]]`.
2. Затем перейти к `[[Go Type System]]`, `[[Go Interfaces]]` и `[[Go Error Handling]]`.
3. После этого читать `[[Go Concurrency Model]]` и его дочерние статьи.
4. Завершить `[[Go Testing]]` как практическую ветку про проверку Go-кода.

## Соседние overview-ветки

- Пока не добавлены, но позже здесь могут появиться соседние language branches.

## Что стоит раскрыть дальше

- [ ] Проверить границы корневой ветки
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
