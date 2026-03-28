
Предлагаемая ветка для `Algorithm Analysis` собирает под одной обзорной рамкой общий аналитический инструмент, алгоритмическую парадигму и прикладное семейство алгоритмов. Для текущего корпуса уже оправдана минимальная структура из `Algorithm Analysis`, `Big O Notation`, `Divide and Conquer` и `Sorting Algorithms`.

## Выбранная оптика

- `area: computer-science`
- `domain: algorithms`
- `section: algorithm-analysis` (предлагаемое новое значение)


## Рекомендуемая иерархия

```text
Algorithm Analysis
├── Big O Notation
├── Divide and Conquer
└── Sorting Algorithms
    ├── Merge Sort
    ├── Quick Sort
    └── Radix Sort
```

## Почему структура именно такая

- `Algorithm Analysis` нужен как корневой `overview`, потому что речь уже идет не об одной статье, а об устойчивом кластере заметок.
- `Big O Notation` не стоит прятать внутрь `Sorting Algorithms`, потому что это общий язык сравнения алгоритмов, а не свойство одной прикладной ветки.
- `Divide and Conquer` тоже должен жить рядом с `Sorting Algorithms`, а не внутри него, потому что это более широкая алгоритмическая парадигма, уже нужная как минимум для `Merge Sort` и `Quick Sort`.
- `Sorting Algorithms` оправдан как отдельный `overview`, потому что внутри него уже есть несколько самостоятельных canonical articles.
- Ветка остается минимальной иерархией без лишних промежуточных уровней.

## Что не стоит создавать заранее

Пока не стоит выносить в отдельные notes:

- `Time Complexity`
- `Space Complexity`
- `Stable Sorting`
- `In-Place Algorithm`

Эти темы пока естественнее раскрывать как разделы внутри `Big O Notation`, `Sorting Algorithms` и отдельных algorithm notes. Их стоит поднимать в самостоятельные узлы только при появлении плотного корпуса связанных заметок.

## Предлагаемое физическое размещение в Inbox

```text
01. Inbox/To Classify/Algorithm Analysis/
├── Algorithm Analysis.md
├── Algorithm Analysis Structure Proposal.md
├── Big O Notation.md
├── Divide and Conquer.md
└── Sorting Algorithms/
    ├── Sorting Algorithms.md
    ├── Merge Sort.md
    ├── Quick Sort.md
    └── Radix Sort.md
```

## Что уже создано в Inbox

- `[[Algorithm Analysis]]`
- `[[Big O Notation]]`
- `[[Divide and Conquer]]`
- `[[Sorting Algorithms]]`
- `[[Merge Sort]]`
- `[[Quick Sort]]`
- `[[Radix Sort]]`

## Про шаблоны

Отдельные тематические template-файлы для `Algorithm Analysis` или `Divide and Conquer` создавать не нужно. По правилам `Principia Rerum` в vault должны оставаться только канонические `Article Template` и `Overview Template`, а предметная специфика должна жить в `frontmatter`, имени заметки и ее содержании.

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: algorithm-analysis`
- [ ] Проверить, когда рядом нужны `Bubble Sort`, `Selection Sort` и `Insertion Sort`
- [ ] Решить, когда `Master Theorem` и `Recurrence Relation` заслужат отдельные notes
- [ ] Проверить `related`
