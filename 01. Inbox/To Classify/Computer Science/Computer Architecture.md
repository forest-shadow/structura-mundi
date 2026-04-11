---
aliases:
  - CPU Architecture
note_type: overview
area: computer-science
domain: computer-architecture
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Operating Systems]]"
  - "[[Compilation]]"
  - "[[Machine Code]]"
  - "[[Instruction Set Architecture (ISA)]]"
  - "[[Microarchitecture]]"
  - "[[Display Technologies]]"
tags: []
---

# Computer Architecture

## Краткое определение области

`Computer Architecture` — это доменная обзорная заметка для веток про программно-видимую и аппаратную организацию вычислительных систем: ISA, модель исполнения инструкций, взаимодействие с памятью, внутреннюю реализацию процессора и аппаратные технологии вывода, через которые машина делает результат вычисления визуально наблюдаемым.

## Что входит в эту тему

- `[[Instruction Set Architecture]]`
- `[[Microarchitecture]]`
- `[[Display Technologies]]`

## Как устроена ветка

- `Instruction Set Architecture` лучше выступает первым устойчивым sub-overview внутри `computer-architecture`, потому что именно через ISA обычно задается программно-видимый контракт между software stack и CPU.
- `Microarchitecture` логично держать sibling-веткой рядом с `Instruction Set Architecture`, потому что именно здесь раскрывается внутренняя организация процессора, реализующая архитектурный контракт через datapath, control logic и execution units.
- `Display Technologies` уместно держать еще одной sibling-веткой внутри `Computer Architecture`, потому что темы вроде `Liquid Crystal Display` описывают не программный контракт и не внутреннюю логику CPU, а аппаратные механизмы визуального вывода результата вычисления.
- Ветка `Computer Architecture` не должна подчиняться ни `Programming Languages`, ни `Operating Systems`, хотя с обеими темами у нее есть плотные поперечные связи.
- Более низкий уровень вроде `Arithmetic Logic Unit`, `Liquid Crystal Display`, `pipeline hazards`, `cache hierarchy` и `memory ordering` стоит выносить в отдельные заметки только по мере появления реального корпуса внутри соответствующей sub-ветки.

## Рекомендуемый маршрут чтения

1. Начать с `[[Instruction Set Architecture]]`, чтобы зафиксировать программно-видимый контракт машины.
2. Затем перейти к `[[Microarchitecture]]`, чтобы увидеть, как этот контракт физически и логически реализуется внутри процессора.
3. После этого перейти к `[[Display Technologies]]`, если нужен аппаратный взгляд на то, как вычислительная система выводит визуальный результат наружу.
4. Затем смотреть поперечные связи с `[[Machine Code]]`, `[[Compilation]]` и `[[Operating Systems]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда внутри `Computer Architecture` нужны отдельные ветки рядом с `Instruction Set Architecture`, `Microarchitecture` и `Display Technologies`
- [ ] Проверить границы между architecture, microarchitecture, display hardware и operating-system-facing mechanisms
- [ ] Проверить `related`
