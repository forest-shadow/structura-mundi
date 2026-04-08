---
aliases:
  - Redox Biology Structure Proposal
  - Структура ветки Redox Biology
note_type: article
area: biology
domain: biochemistry
section: redox-biology
parent:
status: draft
related:
  - "[[Biology]]"
  - "[[Biochemistry]]"
  - "[[Redox Biology]]"
  - "[[Metabolism]]"
  - "[[Antioxidants]]"
tags: []
---

# Redox Biology Structure Proposal

## Краткое определение

Этот файл фиксирует рабочую иерархию заметок для темы `Redox Biology`, в которую естественно помещаются перенос электронов, биологическое окисление, реакционноспособные формы, редокс-гомеостаз и антиоксидантная защита.

## Выбранная оптика

- `area: biology`
- `domain: biochemistry`
- `section: redox-biology`

Почему так:

- `Redox Biology` не стоит оставлять рассыпанной по нескольким несвязанным заметкам прямо под `Biochemistry`, потому что это скрывает общую redox-логику темы;
- `Redox Biology` не стоит подчинять `Nutrition`, потому что dietary antioxidants составляют лишь одну из периферийных линий входа;
- `biochemistry` задает главную disciplinary optic, потому что речь идет о молекулярных механизмах переноса электронов, коферментах, ROS, буферных системах и oxidative stress.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Biochemistry`
- section-level overview: `Redox Biology`

Русскую форму `Редокс-биология` лучше хранить в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Biology
└── Biochemistry
    ├── Metabolism
    └── Redox Biology
        ├── Redox Reactions
        ├── Biological Oxidation
        │   ├── Oxidoreductases
        │   ├── Electron Transfer
        │   ├── Redox Cofactors
        │   │   ├── NAD+/NADH
        │   │   ├── NADP+/NADPH
        │   │   └── FAD/FADH2
        │   ├── Cellular Respiration
        │   │   ├── Electron Transport Chain
        │   │   └── Oxidative Phosphorylation
        │   ├── Peroxisomal Oxidation
        │   └── Cytochrome P450 System
        ├── Reactive Species
        │   ├── Reactive Oxygen Species
        │   ├── Free Radicals
        │   ├── Reactive Nitrogen Species
        │   └── Reactive Sulfur Species
        ├── Redox Homeostasis
        ├── Antioxidants
        ├── Oxidative Stress
        ├── Oxidative Damage
        ├── Repair and Response Systems
        └── Pathophysiological Contexts
```

## Почему структура именно такая

- `Redox Biology` нужна как промежуточная рамка между общим `Biochemistry` и более узкими темами вроде `Antioxidants`, `Oxidative Stress` и `Reactive Oxygen Species`.
- `Antioxidants` лучше рассматривать как часть `Redox Biology`, потому что антиоксидантные системы функционально определяются через redox homeostasis и response to reactive species.
- `Metabolism` остается соседней веткой, потому что метаболизм и редокс-процессы сильно пересекаются, но ни одна из веток не исчерпывает другую.

## Что не стоит делать прямо сейчас

- Не стоит оставлять `Antioxidants` прямой дочерней веткой `Biochemistry`.
- Не стоит заранее создавать полный пакет дочерних canonical notes для всех узлов схемы, пока рядом нет устойчивого корпуса.
- Не стоит сводить `Redox Biology` к dietary antioxidants или nutritional framing.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── Antioxidants.md
├── B/
│   ├── Biology.md
│   └── Biochemistry.md
├── M/
│   └── Metabolism.md
└── R/
    └── Redox Biology.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Biochemistry]]`
- `[[Metabolism]]`
- `[[Antioxidants]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: redox-biology`
- [ ] Решить, какие из дочерних узлов `Redox Biology` действительно пора выносить первыми
- [ ] Проверить границы между `Redox Biology`, `Metabolism` и `Nutrition`
