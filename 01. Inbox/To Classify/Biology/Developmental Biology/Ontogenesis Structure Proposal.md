---
aliases:
  - Ontogenesis Structure Proposal
  - Структура ветки Ontogenesis
note_type: article
area: biology
domain: developmental-biology
section: ontogenesis
parent:
status: draft
related:
  - "[[Biology]]"
  - "[[Developmental Biology]]"
  - "[[Ontogenesis]]"
  - "[[Biochemistry]]"
  - "[[Metabolism]]"
  - "[[Nutrition]]"
tags: []
---

# Ontogenesis Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Ontogenesis`, в которую естественно помещается рассмотрение понятия `онтогенез`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: biology`
- `domain: developmental-biology`
- `section: ontogenesis`

Почему так:

- `Ontogenesis` не стоит встраивать в `biochemistry` как основную рамку, потому что биохимия объясняет механистическую сторону developmental processes, но не задает их главную дисциплинарную оптику;
- `Ontogenesis` не стоит встраивать и в `nutrition`, потому что питание выступает одним из факторов developmental trajectories, а не основной рамкой темы;
- `developmental-biology` лучше задает главную оптику, потому что речь идет об индивидуальном развитии организма, его стадиях, переходах и принципах формирования;
- новый `domain` нужен не для одной заметки, а для устойчивой серии notes о развитии: `Ontogenesis`, `Embryogenesis`, `Morphogenesis`, `Differentiation`, `Growth`, `Maturation`, `Aging`.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Developmental Biology`
- section-level overview: `Ontogenesis`

Русская форма `онтогенез` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Biology
├── Biochemistry
│   └── Metabolism
├── Developmental Biology
│   └── Ontogenesis
└── Nutrition
    └── Vitamins
```

Поперечные связи:

```text
Ontogenesis ↔ Metabolism
Ontogenesis ↔ Nutrition
```

## Почему структура именно такая

- `Developmental Biology` должна быть отдельной domain-root веткой внутри `biology`, потому что без нее темы развития либо окажутся в слишком широкой общей biology-рамке, либо будут искусственно разложены по biochemical и nutritional notes.
- `Ontogenesis` лучше держать как локальный `overview`, а не как простую article-note, потому что тема естественно собирает несколько линий роста: `Embryogenesis`, `Postembryonic Development`, `Growth`, `Maturation`, `Aging`, `Life-Cycle Stages`.
- Не стоит делать отдельный `domain: ontogenesis`, потому что это не disciplinary optic, а центральный кластер внутри более широкой ветки `Developmental Biology`.
- `Metabolism` и `Nutrition` остаются поперечными связями, а не родительскими ветками, потому что они важны для developmental context, но не исчерпывают тему индивидуального развития.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Ontogenesis` ветке `Biochemistry` или `Nutrition`.
- Не стоит заранее создавать большой пакет дочерних notes для `Embryogenesis`, `Morphogenesis`, `Differentiation`, `Growth`, `Maturation` и `Aging`, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельный `domain` под `Ontogenesis`.
- Не стоит создавать отдельные тематические template-файлы под biology или developmental biology: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── B/
│   ├── Biology.md
│   └── Biochemistry.md
├── D/
│   └── Developmental Biology.md
├── M/
│   └── Metabolism.md
├── N/
│   └── Nutrition.md
└── O/
    └── Ontogenesis.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Developmental Biology]]`
- `[[Ontogenesis]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: developmental-biology`
- [ ] Подтвердить `section: ontogenesis`
- [ ] Решить, когда внутри `Ontogenesis` нужны отдельные дочерние статьи
- [ ] Проверить границы между ontogenesis, embryogenesis и life cycle
