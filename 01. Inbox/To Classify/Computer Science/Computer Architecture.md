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
  - "[[Instruction Set Architecture]]"
tags: []
---

# Computer Architecture

## Краткое определение области

`Computer Architecture` — это доменная обзорная заметка для веток про программно-видимую и аппаратную организацию вычислительных систем: ISA, модель исполнения инструкций, взаимодействие с памятью и границу между архитектурным контрактом и конкретной реализацией.

## Что входит в эту тему

- `[[Instruction Set Architecture]]`

## Как устроена ветка

- `Instruction Set Architecture` лучше выступает первым устойчивым sub-overview внутри `computer-architecture`, потому что именно через ISA обычно задается программно-видимый контракт между software stack и CPU.
- Ветка `Computer Architecture` не должна подчиняться ни `Programming Languages`, ни `Operating Systems`, хотя с обеими темами у нее есть плотные поперечные связи.
- Более низкий уровень вроде `microarchitecture`, `pipeline hazards`, `cache hierarchy` и `memory ordering` стоит выносить в отдельные заметки только по мере появления реального корпуса.

## Рекомендуемый маршрут чтения

1. Начать с `[[Instruction Set Architecture]]`.
2. Затем смотреть поперечные связи с `[[Machine Code]]`, `[[Compilation]]` и `[[Operating Systems]]`.
3. После этого, по мере роста ветки, переходить к более локальным architectural-mechanism notes.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда внутри `Computer Architecture` нужны отдельные ветки рядом с `Instruction Set Architecture`
- [ ] Проверить границы между architecture, microarchitecture и operating-system-facing mechanisms
- [ ] Проверить `related`
