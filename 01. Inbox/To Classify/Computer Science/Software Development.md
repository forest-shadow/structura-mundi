---
aliases:
  - Разработка программного обеспечения
  - Developer Tooling
note_type: overview
area: computer-science
domain: software-development
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Computer Science]]"
  - "[[Programming Languages]]"
  - "[[Software Architecture]]"
  - "[[Performance Engineering]]"
  - "[[Vim]]"
tags: []
---

# Software Development

## Краткое определение области

`Software Development` — это domain-root overview для заметок об инструментах, практиках и рабочих средах разработки программного обеспечения: редакторах, version control, build tooling, testing tooling и других инженерных механизмах, через которые разработчик работает с кодом.

## Что входит в эту тему

- `[[Performance Engineering]]`
- `[[Vim]]`

## Как устроена ветка

- `Software Development` собирает не теорию архитектуры и не семантику языков, а именно инструментальный и workflow-слой разработки.
- `Performance Engineering` оправдан как второй section-level overview внутри этого домена, потому что вокруг него естественно группируются profiling, benchmarking, performance-regression analysis и другие практики измерения реального поведения кода.
- `Vim` оправдан как первый section-level overview внутри этого домена, потому что вокруг него уже естественно выделяются modes, motions, operators, text objects, registers, macros и рабочая модель окон и буферов.
- `Software Architecture` остается соседним доменом, потому что описывает организацию системы, а не инструменты редактирования и разработки.
- `Programming Languages` остается соседним доменом, потому что описывает языки и модели выполнения, а не editor-specific практики.

## Рекомендуемый маршрут чтения

1. Если нужен performance-oriented вход, начать с `[[Performance Engineering]]`, затем перейти к `[[Profiling]]`.
2. Если нужен editor/tooling вход, начать с `[[Vim]]`.
3. После этого уже входить в дочерние ветки вроде `[[Profiling Workflow]]`, `[[Vim Modes]]` или `[[Vim Motions]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`
- Соседние домены: `[[Programming Languages]]`, `[[Software Architecture]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `Profiling` нужны `Benchmarking` и `Performance Regression Analysis`
- [ ] Проверить, когда рядом с `Vim` нужны `Git` и build-tooling notes
- [ ] Проверить границу между software development tooling и language-specific toolchains
- [ ] Проверить `related`
