---
aliases:
  - Этномикология Structure Proposal
  - Структура ветки Ethnomycology
note_type: article
area: anthropology
domain: ethnobiology
section: ethnomycology
parent:
status: draft
related:
  - "[[Anthropology]]"
  - "[[Ethnobiology]]"
  - "[[Ethnomycology]]"
tags: []
---

# Ethnomycology Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Ethnomycology` по правилам `Principia Rerum`.

## Выбранная оптика

- `area: anthropology` (новое значение словаря)
- `domain: ethnobiology` (рабочее значение для новой доменной ветки)
- `section: ethnomycology` (рабочее значение для локального кластера)

Почему так:

- `Ethnomycology` неестественно втискивать в существующие `area` вроде `religion`, `history`, `literature` или `linguistics`, потому что тема шире любой одной из этих оптик;
- новая `area` `anthropology` оправдана как отдельная гуманитарная рамка для устойчивого корпуса заметок о культуре, практике, символах и классификациях;
- `Ethnobiology` лучше делать domain-root узлом, потому что `Ethnomycology` является не всей антропологией и не всей ethnobiology, а одной из ее предметных веток;
- `Ethnomycology` лучше держать как section-level overview, а не как обычную `article`, потому что тема естественно распадается на дочерние линии вроде народной классификации грибов, ритуального использования, пищевых практик и культурных установок.

## Канонические имена

- area-level root: `Anthropology`
- domain-root overview: `Ethnobiology`
- section-level overview: `Ethnomycology`

Русские формы `Антропология`, `Этнобиология` и `Этномикология` лучше хранить в `aliases`, а не заводить под них отдельные заметки.

## Рекомендуемая иерархия

```text
Anthropology
└── Ethnobiology
    └── Ethnomycology
```

## Почему структура именно такая

- `Anthropology` должна быть area-level overview, потому что только так новая ветка появляется в системе честно, через изменение закрытого словаря `area`, а не через случайную папку.
- `Ethnobiology` лучше делать первым domain-root внутри `anthropology`, потому что он масштабируется и для соседних тем о культурных отношениях человека с другими частями живого мира.
- `Ethnomycology` оправдана как локальный overview-узел, потому что это уже не единичный термин, а потенциальный кластер заметок.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Ethnomycology` ветке `Religion`, потому что ритуальные и мифологические аспекты здесь важны, но не исчерпывают тему.
- Не стоит размещать тему внутри `History`, потому что историческое измерение здесь вторично по отношению к антропологической оптике.
- Не стоит делать `Ethnomycology` обычной `article-note`, если предполагается дальнейший рост ветки.
- Не стоит создавать отдельные тематические template-файлы под anthropology или ethnobiology: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── Anthropology.md
└── E/
    ├── Ethnobiology.md
    └── Ethnomycology.md
```

## Что уже создано в Inbox

- `[[Anthropology]]`
- `[[Ethnobiology]]`
- `[[Ethnomycology]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда внутри `Ethnomycology` нужны отдельные дочерние статьи
- [ ] Проверить, какие соседние ethnobiological ветки должны появиться рядом
- [ ] Подтвердить `area: anthropology`
- [ ] Подтвердить `domain: ethnobiology`
- [ ] Подтвердить `section: ethnomycology`
