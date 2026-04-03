---
aliases:
  - Vitamins Structure Proposal
  - Структура ветки Vitamins
note_type: article
area: biology
domain: nutrition
section: vitamins
parent:
status: draft
related:
  - "[[Biology]]"
  - "[[Nutrition]]"
  - "[[Vitamins]]"
tags: []
---

# Vitamins Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Vitamins`, в которую естественно помещается рассмотрение понятия `Витамины`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: biology` (новое значение словаря)
- `domain: nutrition` (рабочее значение для новой доменной ветки)
- `section: vitamins` (новый локальный кластер)

Почему так:

- тема `Vitamins` неестественно втискивать в уже существующие `area`, потому что она не является ни исторической, ни литературной, ни религиозной, ни лингвистической темой;
- `medicine` тоже не была бы идеальной корневой рамкой, потому что витамины важны не только как клинический объект, но и как базовая biological и nutritional категория;
- новый `area` `biology` оправдан не одной заметкой: рядом естественно могут появиться ветки про physiology, genetics, microbiology, biochemistry и другие life-science направления;
- `Nutrition` лучше делать domain-root узлом, потому что `Vitamins` являются не всей биологией, а одной из устойчивых nutritional branches;
- `Vitamins` лучше держать как section-level `overview`, потому что тема естественно распадается на дочерние линии вроде fat-soluble vs water-soluble vitamins и отдельных vitamin-specific notes.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Nutrition`
- section-level overview: `Vitamins`

Русская форма `Витамины` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Biology
└── Nutrition
    └── Vitamins
```

## Почему структура именно такая

- `Biology` должна быть area-level overview, потому что новая ветка должна появиться в системе честно, через расширение закрытого словаря `area`.
- `Nutrition` лучше делать первым domain-root внутри `biology`, потому что именно там естественно собираются темы о веществах, поступающих с пищей и поддерживающих физиологические функции организма.
- `Vitamins` оправданы как локальный `overview`, а не как простая article-note, потому что тема уже по своей природе многосоставна.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Vitamins` напрямую под `Biology`, потому что так теряется более точная nutritional рамка.
- Не стоит подчинять `Vitamins` ветке `Medicine`, потому что это создает слишком узкую клиническую оптику.
- Не стоит заранее создавать отдельные canonical notes для каждого витамина, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельные тематические template-файлы под biology или nutrition: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── B/
│   └── Biology.md
├── N/
│   └── Nutrition.md
└── V/
    └── Vitamins.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Nutrition]]`
- `[[Vitamins]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `area: biology`
- [ ] Подтвердить `domain: nutrition`
- [ ] Подтвердить `section: vitamins`
- [ ] Решить, когда внутри `Vitamins` нужны отдельные дочерние статьи
