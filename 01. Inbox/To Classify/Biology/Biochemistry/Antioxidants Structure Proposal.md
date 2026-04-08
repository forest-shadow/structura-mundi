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
  - "[[Redox Biology]]"
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
- `domain: biochemistry`
- `section: antioxidants`

Почему так:

- `Antioxidants` не стоит оставлять прямой дочерней веткой `Biochemistry`, потому что тема естественно раскрывается внутри более широкой рамки переноса электронов, реакционноспособных форм и редокс-гомеостаза;
- `Redox Biology` лучше задает локальную родительскую оптику, потому что антиоксидантные системы являются одной из подсистем общей редокс-регуляции, а не всей темой целиком;
- `Antioxidants` не стоит встраивать в `nutrition` как основную рамку, потому что тема включает не только dietary compounds, но и endogenous biochemical defense systems;
- `biochemistry` по-прежнему задает главную disciplinary optic, потому что речь идет о молекулярных механизмах окисления, антиоксидантной защите, реактивных формах кислорода и клеточных процессах;
- nutritional perspective при этом не теряется, а выражается через поперечные связи с `Nutrition` и `Vitamins`.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Biochemistry`
- section-level overview: `Redox Biology`
- local overview inside redox branch: `Antioxidants`

Русская форма `Антиоксиданты` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Biology
├── Biochemistry
│   └── Redox Biology
│       └── Antioxidants
└── Nutrition
    └── Vitamins
```

Поперечная связь:

```text
Antioxidants ↔ Redox Biology
Antioxidants ↔ Vitamins
Antioxidants ↔ Nutrition
```

## Почему структура именно такая

- `Biochemistry` должна быть отдельной domain-root веткой внутри `biology`, потому что без нее тема антиоксидантов либо окажется в слишком узкой nutritional рамке, либо вообще будет висеть без точной disciplinary perspective.
- `Redox Biology` нужна как промежуточная redox-рамка, чтобы темы о ROS, окислительном стрессе, антиоксидантной защите и редокс-буферах не висели как несвязанный набор sibling-notes прямо под `Biochemistry`.
- `Antioxidants` лучше держать как локальный `overview` внутри `Redox Biology`, а не как простую article-note, потому что тема уже по своей природе собирает несколько разных линий роста.
- `Vitamins` не должны становиться родительской веткой для `Antioxidants`, потому что антиоксидантные свойства некоторых витаминов являются только одним пересечением, а не всей темой целиком.

## Что не стоит делать прямо сейчас

- Не стоит оставлять `Antioxidants` прямой дочерней веткой `Biochemistry`, потому что это скрывает более общую redox-логику темы.
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
├── R/
│   └── Redox Biology.md
└── V/
    └── Vitamins.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Biochemistry]]`
- `[[Antioxidants]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: biochemistry`
- [ ] Подтвердить, что `Antioxidants` живет внутри `Redox Biology`, а не напрямую под `Biochemistry`
- [ ] Решить, когда внутри `Antioxidants` нужны отдельные дочерние статьи
- [ ] Проверить границы между antioxidants, `Redox Biology`, vitamins и oxidative stress
