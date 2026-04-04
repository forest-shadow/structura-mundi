---
aliases:
  - CPU Microarchitecture
note_type: overview
area: computer-science
domain: computer-architecture
section: microarchitecture
parent: "[[Computer Architecture]]"
status: seed
related:
  - "[[Instruction Set Architecture]]"
  - "[[Arithmetic Logic Unit]]"
tags: []
---

# Microarchitecture

## Краткое определение области

`Microarchitecture` — это обзорная заметка для внутренней организации процессора, через которую конкретная аппаратная реализация исполняет архитектурный контракт ISA: datapath, control logic, pipeline, execution units и другие внутренние механизмы.

## Что входит в эту тему

- `[[Arithmetic Logic Unit]]`

## Как устроена ветка

- `Microarchitecture` не совпадает с `Instruction Set Architecture`: ISA задает программно-видимое поведение, а microarchitecture объясняет, как именно процессор реализует это поведение внутри.
- `Arithmetic Logic Unit` логично держать первой дочерней `article`, потому что это один из базовых внутренних вычислительных блоков CPU, но пока не самостоятельная обзорная подветка.
- Отдельные статьи про `Control Unit`, `CPU Pipeline`, `Branch Prediction` или `Register Renaming` стоит добавлять только по мере появления устойчивого корпуса.

## Рекомендуемый маршрут чтения

1. Начать с `[[Computer Architecture]]`.
2. Затем сопоставить `[[Instruction Set Architecture]]` и `Microarchitecture` как два разных уровня описания процессора.
3. После этого перейти к `[[Arithmetic Logic Unit]]` как к первому частному механизму этой ветки.

## Соседние overview-ветки

- Соседний обзорный узел: `[[Instruction Set Architecture]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `Arithmetic Logic Unit` нужны `Control Unit` и `CPU Pipeline`
- [ ] Проверить границы между execution units, datapath и control logic
- [ ] Проверить `related`
