---
aliases:
  - Logic Gates Structure Proposal
  - Структура ветки Logic Gates
note_type: article
area: computer-science
domain: computer-architecture
section: logic-gates
parent:
status: draft
related:
  - "[[Computer Architecture]]"
  - "[[Logic Gates]]"
  - "[[Boolean Logic]]"
  - "[[Truth Table]]"
tags: []
---

# Logic Gates Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Logic Gates`, в которую естественно помещается рассмотрение elementary и primitive gates, включая `NAND Gate` и `NOR Gate`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: computer-architecture`
- `section: logic-gates` (новый локальный кластер)

Почему так:

- `Logic Gates` здесь лучше понимать не как чисто логико-философическую тему, а как ветку про базовые цифровые элементы, реализующие булевы функции на уровне аппаратуры;
- переносить эту тему в `philosophy -> logic` не стоит, потому что там главная оптика - формальная логика, а не схемотехнические примитивы;
- отдельный новый `domain` вроде `digital-electronics` пока преждевременен: для этого в vault еще нет устойчивого корпуса соседних веток.

Поперечные связи с `[[Boolean Logic]]`, `[[Logical Conjunction]]`, `[[Logical Disjunction]]`, `[[Logical Negation]]` и `[[Truth Table]]` должны жить через `related`, а не через родительство.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    └── Logic Gates
        ├── Elementary Logic Gates
        │   ├── NOT Gate
        │   ├── AND Gate
        │   └── OR Gate
        └── Primitive Logic Gates
            ├── NAND Gate
            └── NOR Gate
```

## Почему структура именно такая

- `Logic Gates` оправдан как section-level `overview`, потому что тема уже собирает устойчивый кластер цифровых примитивов, а не одну изолированную definition-note.
- `Elementary Logic Gates` полезен как вложенный `overview`, потому что `NOT`, `AND` и `OR` естественно образуют минимальный базовый набор, на который потом ссылаются производные и универсальные элементы.
- `Primitive Logic Gates` тоже оправдан как вложенный `overview`, если в этой ветке под primitive понимать gates, из которых можно выразить остальные базовые операции; на стартовом этапе достаточно `NAND` и `NOR`.
- Глубже этой вложенности идти пока не стоит: для `transistor-level implementation`, `propagation delay`, `fan-out`, `half adder` и `flip-flop` пока нет отдельного корпуса.

## Что не стоит создавать заранее

- отдельную section-level ветку `Digital Logic`, если в ней пока нет устойчивых sibling-кластеров рядом с `Logic Gates`;
- отдельные canonical notes для `XOR Gate`, `XNOR Gate`, `Buffer Gate` и `Universal Gates`, пока по ним не накопился самостоятельный материал;
- родительство `Logic Gates` под `Boolean Logic`, потому что это смешает формальную и инженерную оптики;
- тематические template-файлы под digital logic: по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── AND Gate.md
├── C/
│   └── Computer Architecture.md
├── E/
│   └── Elementary Logic Gates.md
├── L/
│   └── Logic Gates.md
├── N/
│   ├── NAND Gate.md
│   ├── NOR Gate.md
│   └── NOT Gate.md
├── O/
│   └── OR Gate.md
└── P/
    └── Primitive Logic Gates.md
```

Логическая ветка затем должна собираться через `parent`, а не через физические подпапки.

## Что уже создано в Inbox

- `[[Logic Gates]]`
- `[[Elementary Logic Gates]]`
- `[[Primitive Logic Gates]]`
- `[[NOT Gate]]`
- `[[AND Gate]]`
- `[[OR Gate]]`
- `[[NAND Gate]]`
- `[[NOR Gate]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный overview `Digital Logic`
- [ ] Решить, когда в ветке уместны `XOR Gate` и `XNOR Gate`
- [ ] Добавить в статьи таблицы истинности и краткие схемные примеры
- [ ] Проверить поперечные связи с `Boolean Logic`
