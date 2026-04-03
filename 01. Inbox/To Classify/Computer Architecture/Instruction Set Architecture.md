---
aliases:
  - ISA
note_type: overview
area: computer-science
domain: computer-architecture
section: instruction-set-architecture
parent: "[[Computer Architecture]]"
status: seed
related:
  - "[[Computer Architecture]]"
  - "[[Machine Code]]"
  - "[[Compilation]]"
  - "[[Operating Systems]]"
tags: []
---

# Instruction Set Architecture

## Краткое определение области

`Instruction Set Architecture` — это обзорная заметка для ветки о программно-видимом интерфейсе процессора: наборе инструкций, регистрах, режимах адресации, архитектурных ограничениях и правилах, на которые опираются компиляторы, операционные системы и низкоуровневый код.

## Что входит в эту тему

- instruction set и семантика инструкций;
- архитектурный register model;
- addressing modes;
- instruction encoding;
- privilege-relevant architectural mechanisms, видимые software stack.

## Как устроена ветка

- `Instruction Set Architecture` лучше держать как компактный `overview`, а не как одиночную `article`, потому что тема естественно распадается на несколько самостоятельных аспектов.
- При этом не стоит преждевременно создавать дочерние canonical notes вроде `Instruction Encoding`, `Register File` или `Addressing Modes`, пока рядом нет устойчивого корпуса.
- `Instruction Set Architecture` не должна жить внутри `Compilation`: компилятор только таргетирует ISA, но не задает ее как предметную область.
- `Instruction Set Architecture` не должна жить и внутри `Operating Systems`: ОС использует архитектурный контракт, но не исчерпывает его.

## Рекомендуемый маршрут чтения

1. Начать с `[[Computer Architecture]]`.
2. Затем перейти к `Instruction Set Architecture` как к основному architectural contract between software and CPU.
3. После этого смотреть поперечные связи с `[[Machine Code]]`, `[[Compilation]]` и `[[Operating Systems]]`.

## Соседние overview-ветки

- Пока не добавлены, но позднее рядом могут появиться другие section-level ветки внутри `computer-architecture`.

## Что стоит раскрыть дальше

- [ ] Проверить, какие дочерние статьи действительно нужны внутри `Instruction Set Architecture`
- [ ] Уточнить границы между ISA и microarchitecture
- [ ] Проверить связь с ABI, calling conventions и machine code
- [ ] Проверить `related`
