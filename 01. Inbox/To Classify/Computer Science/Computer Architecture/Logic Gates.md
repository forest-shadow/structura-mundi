---
aliases:
  - Logic Gate
  - Логические элементы
  - Логические вентили
note_type: overview
area: computer-science
domain: computer-architecture
section: logic-gates
parent: "[[Computer Architecture]]"
status: seed
related:
  - "[[Boolean Logic]]"
  - "[[Truth Table]]"
  - "[[Instruction Set Architecture (ISA)]]"
tags: []
---

# Logic Gates

## Краткое определение области

`Logic Gates` - это ветка цифровых аппаратных примитивов, которые реализуют булевы операции над бинарными сигналами и служат базовым строительным материалом для более сложных схем.

## Что входит в эту тему

- `[[Elementary Logic Gates]]` как минимальный набор базовых операций.
- `[[Primitive Logic Gates]]` как кластер универсальных элементов, из которых можно собирать другие gates.

## Как устроена ветка

- `Logic Gates` лучше держать отдельным `overview` внутри `computer-architecture`, потому что здесь главная оптика инженерная, а не чисто логическая.
- `Elementary Logic Gates` собирает базовые операции `NOT`, `AND` и `OR`.
- `Primitive Logic Gates` на стартовом этапе ограничивается `NAND` и `NOR`, чтобы не раздувать ветку без реального корпуса.

## Рекомендуемый маршрут чтения

1. Начать с `[[Elementary Logic Gates]]`, чтобы зафиксировать базовые операции.
2. Затем перейти к `[[Primitive Logic Gates]]`, чтобы увидеть, как `NAND` и `NOR` могут выступать универсальными строительными блоками.
3. После этого полезно сопоставить ветку с `[[Boolean Logic]]` и `[[Truth Table]]`.

## Соседние overview-ветки

- `[[Computer Architecture]]`

## Что стоит раскрыть дальше

- [ ] Добавить краткую границу между symbolic logic и hardware implementation
- [ ] Проверить, нужны ли `XOR Gate` и `XNOR Gate`
- [ ] Добавить примеры построения сложных схем из `NAND` и `NOR`
- [ ] Проверить `related`
