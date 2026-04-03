---
aliases:
  - Computer Architecture Structure Proposal
  - Структура ветки Computer Architecture
note_type: article
area: computer-science
domain: computer-architecture
section:
parent: "[[Computer Science]]"
status: draft
related:
  - "[[Computer Architecture]]"
  - "[[Instruction Set Architecture]]"
  - "[[Compilation]]"
  - "[[Machine Code]]"
  - "[[Operating Systems]]"
tags: []
---

# Computer Architecture Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию domain-root ветки `Computer Architecture` внутри `Computer Science` по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: computer-architecture`
- `section:` пусто у domain-root overview `Computer Architecture`

Почему так:

- тема не укладывается естественно ни в `programming-languages`, ни в `operating-systems`, ни в `software-architecture`;
- для заметок про ISA, memory hierarchy, microarchitecture и CPU-visible execution model нужен собственный предметный фокус;
- `Computer Architecture` описывает весь домен, поэтому не должна получать искусственный `section`.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    └── Instruction Set Architecture
```

## Почему структура именно такая

- `Computer Architecture` оправдана как новый domain-root, потому что без нее `Instruction Set Architecture` пришлось бы помещать в чужую дисциплинарную рамку.
- `Instruction Set Architecture` уже оправдана как первый устойчивый section-level overview внутри домена, потому что через нее естественно раскрываются программно-видимые свойства CPU.
- Поперечные связи с `Compilation`, `Machine Code` и `Operating Systems` важны, но они должны выражаться через `related`, а не через родительство.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Computer Architecture` ветке `Programming Languages` только потому, что компиляторы таргетируют ISA.
- Не стоит подчинять `Computer Architecture` ветке `Operating Systems` только потому, что ОС использует архитектурные механизмы.
- Не стоит заранее создавать sibling-ветки вроде `Microarchitecture`, `Memory Hierarchy` или `Interrupt Architecture`, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельные тематические template-файлы под эту ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── C/
│   └── Computer Architecture.md
└── I/
    └── Instruction Set Architecture.md
```

## Что уже создано в Inbox

- `[[Computer Architecture]]`
- `[[Instruction Set Architecture]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: computer-architecture`
- [ ] Решить, когда рядом с `Instruction Set Architecture` нужны другие section-level ветки
- [ ] Проверить границы между architecture, microarchitecture и OS-facing mechanisms
