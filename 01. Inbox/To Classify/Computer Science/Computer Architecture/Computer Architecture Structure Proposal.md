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
  - "[[Microarchitecture]]"
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
- для заметок про ISA, microarchitecture, memory hierarchy и CPU-visible execution model нужен собственный предметный фокус;
- `Computer Architecture` описывает весь домен, поэтому не должна получать искусственный `section`.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    ├── Instruction Set Architecture
    └── Microarchitecture
        └── Arithmetic Logic Unit
```

## Почему структура именно такая

- `Computer Architecture` оправдана как новый domain-root, потому что без нее `Instruction Set Architecture` пришлось бы помещать в чужую дисциплинарную рамку.
- `Instruction Set Architecture` уже оправдана как первый устойчивый section-level overview внутри домена, потому что через нее естественно раскрываются программно-видимые свойства CPU.
- `Microarchitecture` теперь тоже оправдана как section-level overview внутри того же домена, потому что `Arithmetic Logic Unit` не относится к программно-видимому контракту ISA и требует отдельной оптики на внутреннюю организацию процессора.
- `Arithmetic Logic Unit` лучше держать обычной `article` внутри `Microarchitecture`, а не раздувать отдельный `Execution Units`-overview, пока рядом нет устойчивого корпуса про control unit, load-store units, branch units и FPU.
- Поперечные связи с `Compilation`, `Machine Code` и `Operating Systems` важны, но они должны выражаться через `related`, а не через родительство.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Computer Architecture` ветке `Programming Languages` только потому, что компиляторы таргетируют ISA.
- Не стоит подчинять `Computer Architecture` ветке `Operating Systems` только потому, что ОС использует архитектурные механизмы.
- Не стоит помещать `Arithmetic Logic Unit` внутрь `Instruction Set Architecture`, потому что ALU описывает внутренний механизм исполнения, а не архитектурный контракт, видимый программе.
- Не стоит заранее создавать отдельный overview `Execution Units`, пока рядом нет нескольких самостоятельных sibling-статей кроме `Arithmetic Logic Unit`.
- Не стоит заранее создавать sibling-ветки вроде `Memory Hierarchy` или `Interrupt Architecture`, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельные тематические template-файлы под эту ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── Arithmetic Logic Unit.md
├── C/
│   └── Computer Architecture.md
├── I/
│   └── Instruction Set Architecture.md
└── M/
    └── Microarchitecture.md
```

## Что уже создано в Inbox

- `[[Computer Architecture]]`
- `[[Instruction Set Architecture]]`
- `[[Microarchitecture]]`
- `[[Arithmetic Logic Unit]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: computer-architecture`
- [ ] Подтвердить `section: microarchitecture`
- [ ] Решить, когда рядом с `Instruction Set Architecture` и `Microarchitecture` нужны другие section-level ветки
- [ ] Проверить границы между architecture, microarchitecture и OS-facing mechanisms
