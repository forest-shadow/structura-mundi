---
aliases:
  - Analysis of Algorithms
note_type: overview
area: computer-science
domain: algorithms
section: algorithm-analysis
parent:
status: seed
related:
  - "[[Big O Notation]]"
  - "[[Sorting Algorithms]]"
tags: []
---

# Algorithm Analysis

## Краткое определение области

`Algorithm Analysis` — это обзорная заметка про язык и приемы, с помощью которых сравнивают алгоритмы по росту времени и памяти, а также про устойчивые семейства алгоритмов, где этот анализ особенно важен.

## Что входит в эту тему

- `[[Big O Notation]]`
- `[[Sorting Algorithms]]`

## Как устроена ветка

- `Algorithm Analysis` служит корневой рамкой для всей ветки.
- `Big O Notation` фиксирует общий инструмент асимптотического сравнения.
- `Sorting Algorithms` собирает частную, но крупную подветку алгоритмов, которую удобно читать уже после знакомства с `Big O`.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Algorithm Analysis`.
2. Затем перейти к `[[Big O Notation]]`.
3. После этого читать `[[Sorting Algorithms]]`.
4. Внутри сортировок идти от простых квадратичных алгоритмов к более сильным: `[[Bubble Sort]]`, `[[Selection Sort]]`, `[[Insertion Sort]]`, `[[Merge Sort]]`, `[[Quick Sort]]`, `[[Radix Sort]]`.

## Соседние overview-ветки

- `[[Automata Theory]]` — соседняя обзорная ветка внутри `domain: algorithms`, но про другой смысловой кластер.

## Что стоит раскрыть дальше

- [ ] Уточнить границы между анализом алгоритмов и общей теорией алгоритмов
- [ ] Подтвердить `section: algorithm-analysis`
- [ ] Проверить, нужен ли позже отдельный узел для complexity measures помимо `Big O Notation`
- [ ] Проверить `related`
