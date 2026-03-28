---
aliases: []
note_type: article
area: computer-science
domain: algorithms
section: algorithm-analysis
parent: "[[Algorithms]]"
status: draft
related:
  - "[[Algorithm Analysis]]"
  - "[[Big O Notation]]"
  - "[[Divide and Conquer]]"
  - "[[Sorting Algorithms]]"
tags: []
---

# Algorithm Analysis Structure Proposal

## Краткое определение

Этот файл фиксирует не только желаемую, но и уже фактически существующую смысловую иерархию секции `Algorithm Analysis`. Ветка должна отражать общий аналитический инструмент, прикладную подветку сортировок и общие алгоритмические парадигмы, даже если часть узлов уже существует в `Corpus Mundi`, а часть пока только подготовлена в `Inbox`.

## Выбранная оптика

- `area: computer-science`
- `domain: algorithms`
- `section: algorithm-analysis`

## Текущая смысловая логическая иерархия секции

```text
Algorithm Analysis
├── Big O Notation
├── Divide and Conquer
└── Sorting Algorithms
    ├── Bubble Sort
    ├── Selection Sort
    ├── Insertion Sort
    ├── Merge Sort
    ├── Quick Sort
    └── Radix Sort
```

## Почему иерархия именно такая

- `Algorithm Analysis` остается корневым `overview`, потому что это не одна тема, а обзорная рамка для нескольких устойчивых кластеров.
- `Big O Notation` живет рядом с `Sorting Algorithms`, а не внутри него, потому что это общий язык анализа алгоритмов, а не свойство одной прикладной подветки.
- `Sorting Algorithms` уже оправдан как отдельный `overview`, потому что внутри него существует устойчивый корпус самостоятельных canonical articles.
- `Divide and Conquer` должен быть соседом `Sorting Algorithms`, а не его родителем и не его дочерним узлом: это более широкая алгоритмическая парадигма, которая объясняет `Merge Sort` и `Quick Sort`, но не определяет всю sorting-ветку целиком.
- `Merge Sort` и `Quick Sort` должны сохранять `parent: [[Sorting Algorithms]]`, а связь с `[[Divide and Conquer]]` выражать через содержание и `related`, потому что их основная предметная принадлежность все же sorting, а не общая теория парадигм.

## Что уже существует в Corpus Mundi

В `Corpus Mundi` уже есть следующие notes, которые принадлежат этой секции:

- `[[Algorithm Analysis]]`
- `[[Big O Notation]]`
- `[[Sorting Algorithms]]`
- `[[Bubble Sort]]`
- `[[Selection Sort]]`
- `[[Insertion Sort]]`
- `[[Merge Sort]]`
- `[[Quick Sort]]`
- `[[Radix Sort]]`

Следовательно, логическая иерархия секции уже сейчас обязана учитывать полный sorting-кластер, а не только тот поднабор заметок, который временно лежит в `Inbox`.

## Что сейчас подготовлено в Inbox

В `Inbox` для нормализации и достройки секции сейчас подготовлены:

- `[[Algorithm Analysis]]`
- `[[Big O Notation]]`
- `[[Divide and Conquer]]`
- `[[Sorting Algorithms]]`
- `[[Merge Sort]]`
- `[[Quick Sort]]`
- `[[Radix Sort]]`

На текущем этапе `Divide and Conquer` является новым узлом, который уже нужен смысловой структуре секции, но еще не представлен отдельной canonical note в `Corpus Mundi`.

## Разрыв между логикой и физическим размещением

Физическое размещение файлов в `Corpus Mundi` остается алфавитным и не должно имитировать дерево директорий. Смысловая иерархия секции должна собираться через:

- `parent` для основных вертикальных связей;
- `related` для поперечных содержательных связей;
- обзорные notes вроде `[[Algorithm Analysis]]` и `[[Sorting Algorithms]]`, которые явно называют своих дочерних узлов.

Именно поэтому даже при алфавитном расположении файлов в `Corpus Mundi` логическая ветка секции остается такой:

```text
Algorithm Analysis
├── Big O Notation
├── Divide and Conquer
└── Sorting Algorithms
    ├── Bubble Sort
    ├── Selection Sort
    ├── Insertion Sort
    ├── Merge Sort
    ├── Quick Sort
    └── Radix Sort
```

## Что пока не стоит выносить в отдельные узлы

Пока не стоит создавать отдельные canonical notes только ради полноты схемы:

- `Time Complexity`
- `Space Complexity`
- `Stable Sorting`
- `In-Place Algorithm`
- `Master Theorem`
- `Recurrence Relation`

Эти темы уже смыслово присутствуют в секции, но для самостоятельного статуса им нужен более плотный корпус ссылок и отдельных заметок.

## Про шаблоны

Отдельные тематические template-файлы для `Algorithm Analysis`, `Sorting Algorithms` или `Divide and Conquer` создавать не нужно. По правилам `Principia Rerum` в vault должны оставаться только канонические `Article Template` и `Overview Template`, а предметная специфика должна выражаться через `frontmatter`, имя заметки и ее содержание.

## Следующий шаг

- [ ] Подтвердить `section: algorithm-analysis` как стабильное значение словаря
- [ ] При переносе `Divide and Conquer` в `Corpus Mundi` сохранить его как sibling к `Sorting Algorithms`
- [ ] Проверить `related` у `Merge Sort` и `Quick Sort` после окончательной нормализации
- [ ] При необходимости синхронизировать `[[Algorithm Analysis]]` и `[[Sorting Algorithms]]` в `Corpus Mundi` с этой зафиксированной логической схемой
