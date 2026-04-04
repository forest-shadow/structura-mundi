---
aliases:
  - Universal Logic Gates
note_type: overview
area: computer-science
domain: computer-architecture
section: logic-gates
parent: "[[Logic Gates]]"
status: seed
related:
  - "[[Elementary Logic Gates]]"
  - "[[Truth Table]]"
  - "[[Boolean Logic]]"
tags: []
---

# Primitive Logic Gates

## Краткое определение области

`Primitive Logic Gates` - это кластер gates, которые удобно рассматривать как универсальные строительные элементы: на стартовом этапе сюда входят `NAND Gate` и `NOR Gate`.

## Что входит в эту тему

- `[[NAND Gate]]`
- `[[NOR Gate]]`

## Как устроена ветка

- В этой ветке слово `primitive` используется в практическом смысле: как указание на gates, из которых можно собрать остальные базовые операции.
- Пока не стоит раздувать кластер в отдельную taxonomy для всех derived gates.
- Поперечная связь с `[[Elementary Logic Gates]]` важнее, чем дополнительная внутренняя вложенность.

## Рекомендуемый маршрут чтения

1. Сначала посмотреть `[[NAND Gate]]` как универсальную альтернативу `AND` + `NOT`.
2. Затем перейти к `[[NOR Gate]]` как универсальной альтернативе `OR` + `NOT`.
3. После этого сопоставить их с `[[Elementary Logic Gates]]` и `[[Truth Table]]`.

## Соседние overview-ветки

- `[[Logic Gates]]`
- `[[Elementary Logic Gates]]`

## Что стоит раскрыть дальше

- [ ] Добавить краткое объяснение functional completeness
- [ ] Добавить примеры построения `NOT`, `AND` и `OR` из `NAND` или `NOR`
- [ ] Проверить границу между primitive и derived gates
- [ ] Проверить `related`
