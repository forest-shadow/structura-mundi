---
aliases:
  - Алькебулан Structure Proposal
  - Структура ветки Alkebulan
note_type: article
area: history
domain: african-history
section: names-of-africa
parent: "[[Names of Africa]]"
status: draft
related:
  - "[[History]]"
  - "[[African History]]"
  - "[[Names of Africa]]"
  - "[[Alkebulan]]"
tags: []
---

# Alkebulan Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Alkebulan`, в которую естественно помещается рассмотрение этого понятия по правилам `Principia Rerum`.

## Выбранная оптика

- `area: history`
- `domain: african-history` (предлагаемое новое значение)
- `section: names-of-africa` (предлагаемое новое значение)

Почему так:

- `Alkebulan` неудобно класть напрямую под общий `History`, потому что без отдельной африканской рамки тема теряет предметный контекст;
- делать главной оптикой чистую лингвистику здесь тоже не стоит, потому что в такой заметке важны не только форма слова, но и исторические претензии, контексты употребления и место термина в нарративах об Африке;
- `African History` лучше задает устойчивую domain-root рамку, которая масштабируется не только для `Alkebulan`, но и для других исторических тем об Африке;
- `Names of Africa` оправдана как section-level overview, потому что `Alkebulan` — это не вся African History, а один термин внутри более узкого кластера исторических названий континента.

## Канонические имена

- area-level root: `History`
- domain-root overview: `African History`
- section-level overview: `Names of Africa`
- article: `Alkebulan`

Русская форма `Алькебулан` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
History
└── African History
    └── Names of Africa
        └── Alkebulan
```

## Почему структура именно такая

- `African History` лучше сделать domain-root overview, потому что это естественная рамка для исторических сюжетов, связанных с африканским континентом.
- `Names of Africa` лучше сделать section-level overview, потому что тема `Alkebulan` естественно соседствует с другими историческими именами континента и не должна висеть без локального кластера.
- `Alkebulan` должен быть обычной `article`, а не обзорной заметкой, потому что речь идет об одном конкретном термине, а не о самостоятельной ветке из нескольких уже сложившихся подтем.
- Такая структура сохраняет принцип минимальной глубины: добавляется только один локальный overview-узел, который действительно нужен для осмысленного размещения статьи.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Alkebulan` напрямую под `History`, потому что так пропадает африканский контекст темы.
- Не стоит делать `Alkebulan` section-level overview: для одной статьи это было бы преждевременным разрастанием ветки.
- Не стоит создавать отдельный domain вроде `african-toponymy`, потому что это слишком узкая рамка для текущего корпуса.
- Не стоит создавать отдельные тематические template-файлы под эту ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   ├── African History.md
│   └── Alkebulan.md
├── H/
│   └── History.md
└── N/
    └── Names of Africa.md
```

## Что уже создано в Inbox

- `[[African History]]`
- `[[Names of Africa]]`
- `[[Alkebulan]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Alkebulan` нужны другие статьи о названиях Африки
- [ ] Подтвердить `domain: african-history`
- [ ] Подтвердить `section: names-of-africa`
- [ ] Проверить `related`
