# Algorithm Analysis Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Algorithm Analysis`, в которую естественно помещаются `Big O Notation` и ветка `Sorting Algorithms`, по правилам `Principia Rerum`.

Для этой ветки подходит уже подтвержденная предметная рамка:

- `area: computer-science`
- `domain: algorithms`
- `section: algorithm-analysis` (предлагаемое новое значение)

Такое решение лучше, чем делать `Big O Notation` дочерней заметкой `Sorting Algorithms`, потому что асимптотическая нотация является более общим инструментом анализа, а не частным видом сортировки.

## Канонические имена

- корневая заметка: `Algorithm Analysis`
- подветка: `Sorting Algorithms`
- общий инструмент анализа: `Big O Notation`
- дочерние алгоритмы:
  - `Bubble Sort`
  - `Selection Sort`
  - `Insertion Sort`
  - `Merge Sort`
  - `Quick Sort`
  - `Radix Sort`

Русские названия и альтернативные формулировки лучше хранить в `aliases`, а не в отдельных заметках.

## Рекомендуемая иерархия

```text
Algorithm Analysis (overview)
├── Big O Notation (article)
└── Sorting Algorithms (overview)
    ├── Bubble Sort (article)
    ├── Selection Sort (article)
    ├── Insertion Sort (article)
    ├── Merge Sort (article)
    ├── Quick Sort (article)
    └── Radix Sort (article)
```

## Почему структура именно такая

- `Algorithm Analysis` оправдан как корневой `overview`, потому что здесь есть не одна изолированная тема, а устойчивый кластер из общего инструмента анализа и отдельного семейства алгоритмов.
- `Sorting Algorithms` оправдан как дочерний `sub-overview`, потому что внутри него уже есть несколько самостоятельных алгоритмов, каждый из которых заслуживает собственной canonical article.
- `Big O Notation` лучше держать рядом с `Sorting Algorithms`, а не внутри него: она нужна для сравнения сортировок, но логически шире одной этой ветки.
- Ветка остается минимально вложенной: `root overview -> sub-overview -> article`.

## Что не стоит создавать заранее

Пока не стоит заводить отдельные заметки:

- `Time Complexity`
- `Space Complexity`
- `Stable Sorting`
- `In-Place Algorithm`
- `Divide and Conquer`

Эти темы пока естественнее раскрывать как разделы внутри `Big O Notation`, `Sorting Algorithms` или конкретных статей про алгоритмы. Выносить их в самостоятельные узлы стоит только при появлении устойчивого корпуса заметок.

## Предлагаемое физическое размещение после нормализации

Если ветка будет доведена до канонического состояния, физическое размещение в `Corpus Mundi` должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   └── Algorithm Analysis.md
├── B/
│   ├── Big O Notation.md
│   └── Bubble Sort.md
├── I/
│   └── Insertion Sort.md
├── M/
│   └── Merge Sort.md
├── Q/
│   └── Quick Sort.md
├── R/
│   └── Radix Sort.md
└── S/
    ├── Selection Sort.md
    └── Sorting Algorithms.md
```

Логическая ветка при этом все равно собирается через `parent`, а не через физическое соседство файлов.

## Что создано в Inbox

- `Algorithm Analysis`
- `Big O Notation`
- `Sorting Algorithms`
- `Bubble Sort`
- `Selection Sort`
- `Insertion Sort`
- `Merge Sort`
- `Quick Sort`
- `Radix Sort`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: algorithm-analysis` как новое значение словаря.
2. Наполнить `Big O Notation` и `Sorting Algorithms` так, чтобы корневая ветка уже объясняла различие между инструментом анализа и семейством алгоритмов.
3. После этого повышать зрелость отдельных algorithm notes и решать, какие свойства алгоритмов действительно заслуживают самостоятельных canonical articles.
