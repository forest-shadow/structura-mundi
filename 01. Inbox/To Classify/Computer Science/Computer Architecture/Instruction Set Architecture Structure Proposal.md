---
aliases:
  - ISA Structure Proposal
  - Структура ветки Instruction Set Architecture
note_type: article
area: computer-science
domain: computer-architecture
section: instruction-set-architecture
parent:
status: draft
related:
  - "[[Computer Architecture]]"
  - "[[Instruction Set Architecture (ISA)]]"
  - "[[Compilation]]"
  - "[[Machine Code]]"
  - "[[Operating Systems]]"
tags: []
---

# Instruction Set Architecture Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Instruction Set Architecture`, в которую естественно помещается рассмотрение понятия `ISA`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: computer-architecture` (новое рабочее значение словаря)
- `section: instruction-set-architecture` (новый локальный кластер)

Почему так:

- `Instruction Set Architecture` неестественно втискивать в существующие `domain` вроде `programming-languages` или `operating-systems`, потому что обе ветки лишь используют ISA, но не задают ее как главную предметную оптику;
- новый `domain` `computer-architecture` оправдан не одной заметкой: рядом естественно могут появиться `Microarchitecture`, `Memory Hierarchy`, `Interrupt Architecture`, `CPU Pipeline` и другие sibling-ветки;
- `Instruction Set Architecture` лучше держать как section-level `overview`, потому что тема уже по своей природе собирает несколько устойчивых аспектов, а не одну изолированную definition-note.

## Канонические имена

- domain-root overview: `Computer Architecture`
- section-level overview: `Instruction Set Architecture`

Сокращение `ISA` лучше хранить в `aliases`, а не в отдельной заметке.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    └── Instruction Set Architecture
```

## Почему структура именно такая

- `Computer Architecture` должна быть domain-root заметкой внутри `Computer Science`, потому что здесь нужен самостоятельный предметный фокус, а не подветка чужого домена.
- `Instruction Set Architecture` лучше делать первым устойчивым `overview` внутри этой ветки, потому что именно ISA задает программно-видимый контракт между CPU и software stack.
- `Instruction Set Architecture` не стоит сводить к обычной `article`, если предполагается дальнейший рост ветки вокруг instruction formats, register model, addressing modes и boundary with ABI.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Instruction Set Architecture` заметке `Compilation`, потому что это создает ложную иерархию между target platform contract и compiler workflow.
- Не стоит подчинять `Instruction Set Architecture` ветке `Operating Systems`, потому что ОС лишь опирается на архитектурные механизмы, но не задает саму область.
- Не стоит заранее создавать отдельные canonical notes для `Instruction Encoding`, `Addressing Modes`, `Register Model`, `Privilege Levels` или `Microarchitecture`, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельные тематические template-файлы под computer architecture: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

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
- [ ] Подтвердить `section: instruction-set-architecture`
- [ ] Решить, когда внутри `Instruction Set Architecture` нужны отдельные дочерние статьи
- [ ] Проверить границы между ISA, ABI и microarchitecture
