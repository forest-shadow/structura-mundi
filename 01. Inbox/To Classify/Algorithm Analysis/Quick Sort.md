---
aliases:
  - Quicksort
note_type: article
area: computer-science
domain: algorithms
section: algorithm-analysis
parent: "[[Sorting Algorithms]]"
status: seed
related:
  - "[[Merge Sort]]"
  - "[[Insertion Sort]]"
  - "[[Big O Notation]]"
tags: []
---

# Quick Sort

## Краткое определение

`Quick Sort` — это divide-and-conquer алгоритм сортировки, который выбирает pivot, делит массив на части относительно этого pivot и рекурсивно сортирует получившиеся подмассивы.

## Основная идея или механизм

- выбрать pivot;
- partition вход так, чтобы меньшие элементы оказались слева, а большие справа;
- рекурсивно отсортировать обе части.

## Почему тема находится в ветке Sorting Algorithms

Эта заметка важна как один из главных practically efficient comparison-based sort и как естественный контраст к более предсказуемому `Merge Sort`.

## Профиль сложности

- average case обычно: `O(n log n)`
- worst case: `O(n^2)`
- дополнительная память зависит от рекурсивного стека

## Рабочие свойства и границы темы

- обычно не считается stable в стандартной форме;
- часто хорошо работает in-place по сравнению с `Merge Sort`;
- поведение сильно зависит от partition strategy и выбора pivot.

## Связи с другими заметками

Родительская тема:

`[[Sorting Algorithms]]`

Связанные заметки:

- `[[Merge Sort]]`
- `[[Insertion Sort]]`
- `[[Big O Notation]]`

## Примеры, случаи или следствия

Эта заметка должна показать, почему средний случай и худший случай нельзя смешивать, когда говорят о practical performance `Quick Sort`.

## Что стоит раскрыть дальше

- [ ] Добавить разбор partitioning
- [ ] Развести average case и worst case
- [ ] Зафиксировать роль выбора pivot
- [ ] Проверить `aliases`
