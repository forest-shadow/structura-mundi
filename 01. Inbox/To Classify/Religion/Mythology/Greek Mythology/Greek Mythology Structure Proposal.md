---
aliases:
  - Greek Mythology Structure Proposal
  - Структура ветки Greek Mythology
note_type: article
area: religion
domain: mythology
section: greek-mythology
parent:
status: draft
related:
  - "[[Religion]]"
  - "[[Mythology]]"
  - "[[Greek Mythology]]"
  - "[[Hymenaios]]"
tags: []
---

# Greek Mythology Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Greek Mythology`, в которую естественно помещается рассмотрение такого понятия, как `Hymenaios`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: religion`
- `domain: mythology` (предлагаемое рабочее значение)
- `section: greek-mythology` (предлагаемое рабочее значение)

Почему так:

- `Hymenaios` естественнее читать в религиозно-мифологической, а не исторической или литературной рамке;
- отдельный `domain` `mythology` устойчивее, чем слишком узкий `greek-religion`, потому что он масштабируется и на другие мифологические традиции;
- локальный кластер `greek-mythology` уже достаточно конкретен, чтобы собирать рядом греческих богов, героев и сюжеты, не смешивая их со всем доменом целиком.

## Канонические имена

- area-level root: `Religion`
- domain-root overview: `Mythology`
- section-level overview: `Greek Mythology`
- article: `Hymenaios`

`Гименей`, `Hymen` и `Hymenaeus` лучше хранить в `aliases`, а не заводить под них отдельные заметки.

## Рекомендуемая иерархия

```text
Religion
└── Mythology
    └── Greek Mythology
        └── Hymenaios
```

## Почему структура именно такая

- `Religion` лучше фиксировать как area-level overview, потому что это уже утвержденная область знания в словаре `area`.
- `Mythology` оправдана как первый domain-root внутри `religion`, потому что здесь нужен не одиночный контейнер под одного персонажа, а рамка для устойчивой серии заметок о мифологических системах.
- `Greek Mythology` лучше сделать section-level overview, потому что `Hymenaios` не существует как абстрактное божество вне конкретной традиции; его естественный контекст — древнегреческий мифологический корпус.
- `Hymenaios` должен быть обычной `article`, а не обзорной заметкой, потому что речь идет о конкретной фигуре, а не о ветке из нескольких самостоятельных подтем.

## Что не стоит делать прямо сейчас

- Не стоит класть `Hymenaios` напрямую под `Religion`, потому что так теряется мифологическая и культурная рамка.
- Не стоит заранее вводить промежуточный overview вроде `Greek Gods` или `Wedding Deities`, пока рядом нет реального корпуса sibling-заметок.
- Не стоит создавать отдельные тематические template-файлы под религию или мифологию: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── G/
│   └── Greek Mythology.md
├── H/
│   └── Hymenaios.md
├── M/
│   └── Mythology.md
└── R/
    └── Religion.md
```

## Что уже создано в Inbox

- `[[Religion]]`
- `[[Mythology]]`
- `[[Greek Mythology]]`
- `[[Hymenaios]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Hymenaios` нужны другие статьи о греческих божествах
- [ ] Проверить, нужен ли отдельный sub-overview только после появления нескольких sibling-заметок
- [ ] Подтвердить `domain: mythology`
- [ ] Подтвердить `section: greek-mythology`
