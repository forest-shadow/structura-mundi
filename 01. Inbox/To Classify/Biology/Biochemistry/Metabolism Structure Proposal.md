---
aliases:
  - Metabolism Structure Proposal
  - Структура ветки Metabolism
note_type: article
area: biology
domain: biochemistry
section: metabolism
parent:
status: draft
related:
  - "[[Biology]]"
  - "[[Biochemistry]]"
  - "[[Metabolism]]"
  - "[[Nutrition]]"
  - "[[Redox Biology]]"
  - "[[Antioxidants]]"
tags: []
---

# Metabolism Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Metabolism`, в которую естественно помещается рассмотрение понятия `Метаболизм`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: biology`
- `domain: biochemistry`
- `section: metabolism`

Почему так:

- `Metabolism` не стоит встраивать в `nutrition` как основную рамку, потому что питание описывает поступление, усвоение и обеспечение организма веществами, а метаболизм описывает все внутренние биохимические превращения этих веществ;
- `biochemistry` лучше задает главную оптику, потому что речь идет о ферментативных реакциях, энергетическом обмене, метаболических путях и их регуляции;
- nutritional perspective при этом не теряется, а выражается через поперечную связь с `Nutrition`;
- `Metabolism` уже достаточно широк, чтобы быть отдельным локальным кластером, а не одной из строк внутри общего `Biochemistry`.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Biochemistry`
- section-level overview: `Metabolism`

Русские формы `Метаболизм` и `Обмен веществ` лучше хранить в `aliases`, а не в отдельных параллельных заметках.

## Рекомендуемая иерархия

```text
Biology
├── Biochemistry
│   ├── Metabolism
│   └── Redox Biology
│       └── Antioxidants
└── Nutrition
    └── Vitamins
```

Поперечные связи:

```text
Metabolism ↔ Nutrition
Metabolism ↔ Redox Biology
```

## Почему структура именно такая

- `Metabolism` лучше держать как локальный `overview`, а не как простую article-note, потому что тема естественно распадается на несколько линий роста: `Anabolism`, `Catabolism`, `Energy Metabolism`, `Metabolic Pathways`, `Metabolic Regulation`.
- Не стоит делать отдельный `domain: metabolism`, потому что для текущего корпуса это не самостоятельная disciplinary optic, а центральный кластер внутри уже созданной ветки `Biochemistry`.
- Не стоит подчинять `Metabolism` ветке `Nutrition`, потому что это сместит тему в сторону nutrient input и dietary context, хотя метаболизм существенно шире этой рамки.
- `Redox Biology` лучше держать соседней, а не дочерней веткой, потому что редокс-процессы пересекаются с метаболизмом, но не исчерпываются им; внутри этой ветки уже естественно помещаются `Antioxidants`.

## Что не стоит делать прямо сейчас

- Не стоит создавать отдельный `domain` под `Metabolism`.
- Не стоит заранее создавать большой пакет дочерних notes для `Anabolism`, `Catabolism`, `Glycolysis`, `Citric Acid Cycle`, `Oxidative Phosphorylation` и `Metabolic Regulation`, пока рядом нет устойчивого корпуса.
- Не стоит переносить `Metabolism` в `Nutrition`, даже если многие nutritional notes будут на него ссылаться.
- Не стоит создавать отдельные тематические template-файлы под biology или biochemistry: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── B/
│   ├── Biology.md
│   └── Biochemistry.md
├── M/
│   └── Metabolism.md
├── R/
│   └── Redox Biology.md
├── A/
│   └── Antioxidants.md
└── N/
    └── Nutrition.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Biochemistry]]`
- `[[Metabolism]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: metabolism`
- [ ] Решить, когда внутри `Metabolism` нужны отдельные дочерние статьи
- [ ] Проверить границы между metabolism, nutrition и bioenergetics
- [ ] Проверить поперечные связи с `Redox Biology`
