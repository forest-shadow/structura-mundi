---
aliases:
  - Antioxidants Structure Proposal
  - Структура ветки Antioxidants
note_type: article
area: biology
domain: biochemistry
section: antioxidants
parent:
status: draft
related:
  - "[[Biology]]"
  - "[[Biochemistry]]"
  - "[[Antioxidants]]"
  - "[[Nutrition]]"
  - "[[Vitamins]]"
tags: []
---

# Antioxidants Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Antioxidants`, в которую естественно помещается рассмотрение понятия `Антиоксиданты`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: biology`
- `domain: biochemistry` (новое рабочее значение словаря)
- `section: antioxidants` (новый локальный кластер)

Почему так:

- `Antioxidants` не стоит встраивать в `nutrition` как основную рамку, потому что тема включает не только dietary compounds, но и endogenous biochemical defense systems;
- `biochemistry` лучше задает главную оптику, потому что речь идет о молекулярных механизмах окисления, антиоксидантной защите, реактивных формах кислорода и клеточных процессах;
- nutritional perspective при этом не теряется, а выражается через поперечные связи с `Nutrition` и `Vitamins`.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Biochemistry`
- section-level overview: `Antioxidants`

Русская форма `Антиоксиданты` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Biology
├── Biochemistry
│   └── Antioxidants
└── Nutrition
    └── Vitamins
```

Поперечная связь:

```text
Antioxidants ↔ Vitamins
Antioxidants ↔ Nutrition
```

## Почему структура именно такая

- `Biochemistry` должна быть отдельной domain-root веткой внутри `biology`, потому что без нее тема антиоксидантов либо окажется в слишком узкой nutritional рамке, либо вообще будет висеть без точной disciplinary perspective.
- `Antioxidants` лучше держать как локальный `overview`, а не как простую article-note, потому что тема уже по своей природе собирает несколько разных линий роста.
- `Vitamins` не должны становиться родительской веткой для `Antioxidants`, потому что антиоксидантные свойства некоторых витаминов являются только одним пересечением, а не всей темой целиком.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Antioxidants` ветке `Nutrition`, потому что это исказит тему в сторону only dietary substances.
- Не стоит подчинять `Antioxidants` ветке `Vitamins`, потому что не все антиоксиданты являются витаминами и не все аспекты темы сводятся к микронутриентам.
- Не стоит заранее создавать отдельные canonical notes для `Oxidative Stress`, `Reactive Oxygen Species`, `Glutathione`, `Catalase`, `Superoxide Dismutase`, `Vitamin C` и `Vitamin E`, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельные тематические template-файлы под biology или biochemistry: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── Antioxidants.md
├── B/
│   ├── Biology.md
│   └── Biochemistry.md
├── N/
│   └── Nutrition.md
└── V/
    └── Vitamins.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Biochemistry]]`
- `[[Antioxidants]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: biochemistry`
- [ ] Подтвердить `section: antioxidants`
- [ ] Решить, когда внутри `Antioxidants` нужны отдельные дочерние статьи
- [ ] Проверить границы между antioxidants, vitamins и oxidative stress
