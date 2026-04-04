---
aliases:
  - CPU Register Structure Proposal
  - Структура ветки Register
note_type: article
area: computer-science
domain: computer-architecture
section: instruction-set-architecture
parent: "[[Instruction Set Architecture]]"
status: draft
related:
  - "[[Computer Architecture]]"
  - "[[Instruction Set Architecture]]"
  - "[[Machine Code]]"
  - "[[Compilation]]"
  - "[[Operating Systems]]"
tags: []
---

# Register Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Instruction Set Architecture`, в которую естественно помещается рассмотрение такого понятия, как `Register`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: computer-architecture`
- `section: instruction-set-architecture`

Почему так:

- в контексте hardware и CPU понятие `Register` относится прежде всего к программно-видимому архитектурному состоянию процессора;
- существующая ветка `Instruction Set Architecture` уже задает корректную рамку для таких сущностей, как регистры, режимы адресации, форматы инструкций и privilege-relevant state;
- для одной статьи про `Register` не нужен отдельный новый `section` и не нужен новый `domain`;
- поперечные связи с `Compilation`, `Machine Code` и `Operating Systems` важны, но они не отменяют того, что главная предметная оптика здесь именно архитектурная.

## Канонические имена

- domain-root overview: `Computer Architecture`
- section-level overview: `Instruction Set Architecture`
- article: `Register`

`CPU Register`, `Processor Register`, `Architectural Register` и `Регистр процессора` лучше хранить в `aliases`, а не раскладывать по отдельным заметкам.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    └── Instruction Set Architecture
        └── Register
```

## Почему структура именно такая

- `Register` лучше делать обычной `article`, а не новым `overview`, потому что на текущем этапе это один конкретный архитектурный термин, а не разросшаяся самостоятельная подветка.
- `Register` естественно подчиняется `Instruction Set Architecture`, потому что ISA определяет регистровую модель, архитектурно видимое состояние и семантику инструкций, воздействующих на регистры.
- Более частные сущности вроде `Program Counter`, `Status Register`, `General-Purpose Register`, `Control/Status Register` и `Register File` при необходимости могут позже стать sibling-статьями внутри той же ветки, не требуя промежуточного искусственного уровня.
- Такая структура сохраняет принцип минимальной глубины: логическая иерархия остается ясной, но не разрастается раньше времени.

## Что не стоит делать прямо сейчас

- Не стоит создавать промежуточный `overview` вроде `Register Model` или `CPU Registers`, пока рядом нет устойчивого корпуса дочерних статей.
- Не стоит подчинять `Register` ветке `Compilation` только потому, что компиляторы делают register allocation.
- Не стоит подчинять `Register` ветке `Operating Systems` только потому, что ОС использует privileged registers и сохраняет регистровое состояние при переключении контекста.
- Не стоит создавать отдельные тематические template-файлы под `computer-architecture` или `Instruction Set Architecture`: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`, а рабочие заготовки лучше создавать сразу как конкретные заметки.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── C/
│   └── Computer Architecture.md
├── I/
│   └── Instruction Set Architecture.md
└── R/
    └── Register.md
```

## Что уже создано в Inbox

- `[[Instruction Set Architecture]]`
- `[[Register]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Register` нужны отдельные статьи `Program Counter` и `Status Register`
- [ ] Проверить, когда оправдан отдельный обзорный узел только для register model
- [ ] Уточнить границу между architectural registers и physical registers
- [ ] Проверить связь с `Register File` и `register allocation`
- [ ] Проверить `related`
