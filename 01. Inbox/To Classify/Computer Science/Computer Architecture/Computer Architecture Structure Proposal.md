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
  - "[[Instruction Set Architecture (ISA)]]"
  - "[[Microarchitecture]]"
  - "[[Display Technologies]]"
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
- для заметок про ISA, microarchitecture, memory hierarchy, display hardware и CPU-visible execution model нужен собственный предметный фокус;
- `Computer Architecture` описывает весь домен, поэтому не должна получать искусственный `section`.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    ├── Instruction Set Architecture
    ├── Microarchitecture
    │   └── Arithmetic Logic Unit
    └── Display Technologies
        └── Liquid Crystal Display
```

## Почему структура именно такая

- `Computer Architecture` оправдана как новый domain-root, потому что без нее `Instruction Set Architecture`, `Microarchitecture` и display-oriented hardware пришлось бы помещать в чужую дисциплинарную рамку.
- `Instruction Set Architecture` уже оправдана как section-level overview внутри домена, потому что через нее естественно раскрываются программно-видимые свойства CPU.
- `Microarchitecture` тоже оправдана как section-level overview внутри того же домена, потому что `Arithmetic Logic Unit` не относится к программно-видимому контракту ISA и требует отдельной оптики на внутреннюю организацию процессора.
- `Display Technologies` нужна как section-level overview, потому что `Liquid Crystal Display` неудобно оставлять изолированной article-note без общего узла для sibling-технологий вроде `OLED`, `CRT` и `E Ink`.
- `Liquid Crystal Display` пока лучше держать обычной `article` внутри `Display Technologies`, а не раздувать отдельный LCD-specific overview, пока рядом нет устойчивого корпуса про panel types, backlighting families и manufacturing variants.
- Поперечные связи с `Compilation`, `Machine Code` и `Operating Systems` важны, но они должны выражаться через `related`, а не через родительство.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Computer Architecture` ветке `Programming Languages` только потому, что компиляторы таргетируют ISA.
- Не стоит подчинять `Computer Architecture` ветке `Operating Systems` только потому, что ОС использует архитектурные механизмы.
- Не стоит помещать `Arithmetic Logic Unit` внутрь `Instruction Set Architecture`, потому что ALU описывает внутренний механизм исполнения, а не архитектурный контракт, видимый программе.
- Не стоит заранее создавать sibling-ветки вроде `Memory Hierarchy` или `Interrupt Architecture`, пока рядом нет устойчивого корпуса.
- Не стоит заранее создавать отдельный `domain` вроде `display-engineering` или `digital-electronics`, пока display-темы представлены только начальным кластером.
- Не стоит создавать отдельный overview вроде `Flat-Panel Displays` или LCD-specific template-файлы: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── Arithmetic Logic Unit.md
├── C/
│   └── Computer Architecture.md
├── D/
│   └── Display Technologies.md
├── I/
│   └── Instruction Set Architecture.md
├── L/
│   └── Liquid Crystal Display.md
└── M/
    └── Microarchitecture.md
```

## Что уже создано в Inbox

- `[[Computer Architecture]]`
- `[[Instruction Set Architecture]]`
- `[[Microarchitecture]]`
- `[[Arithmetic Logic Unit]]`
- `[[Display Technologies]]`
- `[[Liquid Crystal Display]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: computer-architecture`
- [ ] Подтвердить `section: display-technologies`
- [ ] Решить, когда рядом с `Instruction Set Architecture`, `Microarchitecture` и `Display Technologies` нужны другие section-level ветки
- [ ] Проверить границы между architecture, microarchitecture, display hardware и OS-facing mechanisms
