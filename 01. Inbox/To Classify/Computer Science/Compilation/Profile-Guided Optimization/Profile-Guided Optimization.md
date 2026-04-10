---
aliases:
  - PGO
  - Profile Guided Optimization
note_type: overview
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Compilation]]"
  - "[[Program Translation Pipeline]]"
  - "[[Go Profile-Guided Optimization]]"
  - "[[Go pprof]]"
  - "[[Profile-Guided Optimization Profile Collection]]"
  - "[[Profile-Guided Optimization Feedback Loop]]"
  - "[[Profile-Guided Optimization Constraints and Trade-offs]]"
tags: []
---

# Profile-Guided Optimization

## Краткое определение области

`Profile-Guided Optimization` - это overview-узел о подходе к оптимизации компиляции, в котором решения компилятора опираются на профильные данные реального или репрезентативного выполнения программы.

## Что входит в эту тему

- `[[Profile-Guided Optimization Profile Collection]]`
- `[[Profile-Guided Optimization Feedback Loop]]`
- `[[Profile-Guided Optimization Constraints and Trade-offs]]`

## Как устроена ветка

- `Profile-Guided Optimization` живёт внутри `[[Compilation]]`, потому что речь идёт о cross-language compiler optimization workflow, а не о language-specific runtime-диагностике.
- `Profile-Guided Optimization Profile Collection` удерживает вопрос, откуда берутся профильные данные и какие workload assumptions за ними стоят.
- `Profile-Guided Optimization Feedback Loop` удерживает путь от profile data к повторной сборке и изменению optimization decisions.
- `Profile-Guided Optimization Constraints and Trade-offs` удерживает ограничения, риски и стоимость применения PGO.

## Рекомендуемый маршрут чтения

1. Начать с `[[Profile-Guided Optimization Profile Collection]]`.
2. Затем перейти к `[[Profile-Guided Optimization Feedback Loop]]`.
3. После этого читать `[[Profile-Guided Optimization Constraints and Trade-offs]]`.
4. Для language-specific случая сопоставлять с `[[Go Profile-Guided Optimization]]`.

## Соседние overview-ветки

- `[[Compilation]]`
- `[[Go Profile-Guided Optimization]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про instrumentation-based и sampling-based PGO
- [ ] Уточнить границу между PGO, JIT-профилированием и runtime-adaptive optimization
- [ ] Проверить `related`
