---
aliases:
  - Sorting
note_type: overview
area: computer-science
domain: algorithms
section: algorithm-analysis
parent: "[[Algorithm Analysis]]"
status: seed
related:
  - "[[Big O Notation]]"
  - "[[Bubble Sort]]"
  - "[[Insertion Sort]]"
  - "[[Merge Sort]]"
  - "[[Quick Sort]]"
  - "[[Radix Sort]]"
tags: []
---

# Sorting Algorithms

## Краткое определение области

`Sorting Algorithms` — это обзорная заметка про класс алгоритмов, которые упорядочивают набор элементов по выбранному критерию и потому естественно сравниваются по времени, памяти и дополнительным свойствам вроде стабильности и работы in-place.

## Что входит в эту тему

- `[[Bubble Sort]]`
- `[[Selection Sort]]`
- `[[Insertion Sort]]`
- `[[Merge Sort]]`
- `[[Quick Sort]]`
- `[[Radix Sort]]`

## Как устроена ветка

- `Bubble Sort`, `Selection Sort` и `Insertion Sort` удобно держать как стартовые простые алгоритмы с квадратичным временем в типичном общем случае.
- `Merge Sort` и `Quick Sort` образуют более сильную подветку эффективных comparison-based sort.
- `Radix Sort` важно держать рядом с ними, но отдельно проговаривать, что это уже не comparison-based подход в обычном смысле.

## Рекомендуемый маршрут чтения

1. Сначала прочитать `[[Big O Notation]]`.
2. Затем пройти простые алгоритмы: `[[Bubble Sort]]`, `[[Selection Sort]]`, `[[Insertion Sort]]`.
3. После этого перейти к `[[Merge Sort]]` и `[[Quick Sort]]`.
4. В конце читать `[[Radix Sort]]`, чтобы отдельно увидеть границу между comparison-based и non-comparison sorting.

## Соседние overview-ветки

- Родительская рамка: `[[Algorithm Analysis]]`

## Что стоит раскрыть дальше

- [ ] Добавить явное сравнение comparison-based и non-comparison sorting
- [ ] Решить, нужен ли позже отдельный узел про sorting properties
- [ ] Проверить, не просится ли позже отдельная заметка про partitioning
- [ ] Проверить `related`
