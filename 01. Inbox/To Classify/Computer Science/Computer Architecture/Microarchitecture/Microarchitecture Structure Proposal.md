---
aliases:
  - Microarchitecture Structure Proposal
  - Структура ветки Microarchitecture
note_type: article
area: computer-science
domain: computer-architecture
section: microarchitecture
parent:
status: draft
related:
  - "[[Computer Architecture]]"
  - "[[Microarchitecture]]"
  - "[[Instruction Set Architecture]]"
  - "[[Arithmetic Logic Unit]]"
tags: []
---

# Microarchitecture Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Microarchitecture`, в которую естественно помещается рассмотрение понятия `ALU`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: computer-architecture`
- `section: microarchitecture` (новый локальный кластер)

Почему так:

- `ALU` неестественно помещать в `instruction-set-architecture`, потому что это не программно-видимый контракт, а внутренний механизм исполнения инструкций;
- внутри `computer-architecture` уже есть естественное смысловое разделение между внешним архитектурным интерфейсом машины и ее внутренней реализацией;
- новый `section` `microarchitecture` оправдан не одной заметкой: рядом естественно могут появиться `Control Unit`, `CPU Pipeline`, `Branch Prediction`, `Register Renaming`, `Reorder Buffer` и другие sibling-темы;
- `Microarchitecture` лучше держать section-level `overview`, потому что тема уже по своей природе собирает несколько потенциальных внутренних механизмов, а не одну isolated definition-note.

## Канонические имена

- domain-root overview: `Computer Architecture`
- section-level overview: `Microarchitecture`
- article: `Arithmetic Logic Unit`

Сокращение `ALU` лучше хранить в `aliases`, а не в отдельной заметке.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    ├── Instruction Set Architecture
    └── Microarchitecture
        └── Arithmetic Logic Unit
```

## Почему структура именно такая

- `Microarchitecture` нужна как отдельный `overview`, потому что иначе `ALU` пришлось бы либо ошибочно подчинять `Instruction Set Architecture`, либо оставлять без устойчивого обзорного узла.
- `Arithmetic Logic Unit` пока лучше держать обычной `article`, потому что сама по себе ALU еще не образует локальный обзорный кластер, а является одним из первых фундаментальных механизмов внутри microarchitecture.
- Глубже идти не стоит, пока рядом нет корпуса заметок про разные execution units или внутренние стадии процессора.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельную каноническую заметку `ALU`, если она будет просто дублировать `Arithmetic Logic Unit` под сокращенным именем.
- Не стоит помещать `Arithmetic Logic Unit` внутрь `Instruction Set Architecture`, потому что это смешивает архитектурный контракт и внутреннюю реализацию.
- Не стоит заранее вводить отдельный `overview` `Execution Units`, пока кроме `Arithmetic Logic Unit` рядом нет устойчивого набора sibling-статей.
- Не стоит создавать тематические template-файлы под microarchitecture: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

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

Логическая ветка при этом собирается через `parent`, а не через вложенные папки.

## Созданные seed-заготовки

- `Microarchitecture.md`
- `Arithmetic Logic Unit.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: microarchitecture`.
2. Решить, когда рядом с `Arithmetic Logic Unit` нужны `Control Unit` и `CPU Pipeline`.
3. Уточнить границы между `Instruction Set Architecture` и `Microarchitecture`.
4. Проверить, не нужен ли позднее отдельный article про `Execution Unit` как более общий термин.
