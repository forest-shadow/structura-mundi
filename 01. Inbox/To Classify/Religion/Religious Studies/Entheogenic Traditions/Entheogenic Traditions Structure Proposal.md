---
aliases:
  - Entheogenic Traditions Structure Proposal
  - Структура ветки Entheogenic Traditions
note_type: article
area: religion
domain: religious-studies
section: entheogenic-traditions
parent:
status: draft
related:
  - "[[Religion]]"
  - "[[Religious Studies]]"
  - "[[Entheogenic Traditions]]"
  - "[[Entheomycology]]"
tags: []
---

# Entheogenic Traditions Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Entheogenic Traditions`, в которую естественно помещается рассмотрение такого понятия, как `Entheomycology`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: religion`
- `domain: religious-studies` (предлагаемое новое значение)
- `section: entheogenic-traditions` (предлагаемое новое значение)

Почему так:

- `Entheomycology` описывает не мифологический корпус, а исследовательскую и религиоведческую оптику на сакральное и ритуальное использование грибов;
- существующий `domain: mythology` здесь слишком узок и искажает тему, потому что сводит ее к мифам, а не к практикам, опытам и сравнительному анализу;
- `religious-studies` полезен не для одной заметки, а для серии тем о ритуале, сакральных посредниках, экстатических практиках и религиозных технологиях опыта;
- `section: entheogenic-traditions` достаточно узок, чтобы собирать рядом заметки об энтеогенах в религиозном контексте, но не сводить ветку только к грибам.

## Канонические имена

- area-level root: `Religion`
- domain-root overview: `Religious Studies`
- section-level overview: `Entheogenic Traditions`
- article: `Entheomycology`

`Энтеомикология` лучше хранить в `aliases`, а не делать отдельным русскоязычным файлом.

## Рекомендуемая иерархия

```text
Religion
└── Religious Studies
    └── Entheogenic Traditions
        └── Entheomycology
```

## Почему структура именно такая

- `Religion` уже существует как area-level overview, поэтому новый верхний уровень создавать не нужно.
- `Religious Studies` лучше сделать domain-root overview, потому что здесь нужна дисциплинарная рамка для тем, которые описывают религиозные практики и режимы сакрального опыта, а не мифологические персонажи и сюжеты.
- `Entheogenic Traditions` лучше сделать section-level overview, потому что это уже не один термин, а потенциальный кластер заметок о сакраментальном использовании энтеогенов, сравнительных ритуальных контекстах и формах религиозного посредничества.
- `Entheomycology` должен быть обычной `article`, а не overview, потому что на текущем этапе речь идет о конкретном понятии и исследовательской оптике, а не о разросшейся отдельной подветке.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Entheomycology` напрямую под `Religion`, потому что так теряется религиоведческая рамка.
- Не стоит относить `Entheomycology` к `Mythology`, потому что тема не исчерпывается мифами и не должна быть классифицирована как мифологический корпус.
- Не стоит заранее вводить промежуточный overview вроде `Sacred Fungi` или `Mushroom Cults`, пока рядом нет устойчивого корпуса sibling-заметок.
- Не стоит создавать отдельные тематические template-файлы под религиоведение, энтеогены или энтеомикологию: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── E/
│   ├── Entheogenic Traditions.md
│   └── Entheomycology.md
└── R/
    └── Religious Studies.md
```

## Что уже создано в Inbox

- `[[Religious Studies]]`
- `[[Entheogenic Traditions]]`
- `[[Entheomycology]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Entheomycology` нужны отдельные статьи про `Entheogen` и `Sacred Fungi`
- [ ] Проверить, когда ветке нужен sub-overview только по грибным энтеогенам
- [ ] Подтвердить `domain: religious-studies`
- [ ] Подтвердить `section: entheogenic-traditions`
- [ ] Проверить `related`
