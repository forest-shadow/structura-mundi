---
aliases:
  - Phylogenesis Structure Proposal
  - Структура ветки Phylogenesis
note_type: article
area: biology
domain: evolutionary-biology
section: phylogenesis
parent:
status: draft
related:
  - "[[Biology]]"
  - "[[Evolutionary Biology]]"
  - "[[Phylogenesis]]"
  - "[[Developmental Biology]]"
  - "[[Ontogenesis]]"
tags: []
---

# Phylogenesis Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Phylogenesis`, в которую естественно помещается рассмотрение понятия `филогенез`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: biology`
- `domain: evolutionary-biology`
- `section: phylogenesis`

Почему так:

- `Phylogenesis` не стоит встраивать в `developmental-biology` как основную рамку, потому что биология развития описывает индивидуальное развитие организма, а филогенез — историческое развитие линии или группы организмов;
- `Phylogenesis` не стоит держать и просто внутри общей `biology`, потому что тема требует отдельной evolutionary perspective;
- `evolutionary-biology` лучше задает главную оптику, потому что речь идет о происхождении таксонов, общих предках, эволюционном расхождении и длительных исторических траекториях;
- новый `domain` нужен не для одной заметки, а для устойчивой серии notes о происхождении и расхождении линий: `Phylogenesis`, `Speciation`, `Cladogenesis`, `Common Ancestry`, `Homology`, `Phylogenetic Trees`.

## Канонические имена

- area-level root: `Biology`
- domain-root overview: `Evolutionary Biology`
- section-level overview: `Phylogenesis`

Русская форма `филогенез` лучше хранится в `aliases`, а не в отдельной параллельной заметке.

## Рекомендуемая иерархия

```text
Biology
├── Developmental Biology
│   └── Ontogenesis
├── Evolutionary Biology
│   └── Phylogenesis
└── Biochemistry
    └── Metabolism
```

Поперечные связи:

```text
Phylogenesis ↔ Ontogenesis
Phylogenesis ↔ Developmental Biology
```

## Почему структура именно такая

- `Evolutionary Biology` должна быть отдельной domain-root веткой внутри `biology`, потому что без нее темы филогенеза, происхождения групп и эволюционных линий будут либо висеть в слишком широкой общей biology-рамке, либо искусственно тянуться в `Developmental Biology`.
- `Phylogenesis` лучше держать как локальный `overview`, а не как простую article-note, потому что тема естественно собирает несколько линий роста: `Speciation`, `Cladogenesis`, `Common Ancestry`, `Phylogenetic Trees`, `Homology`, `Evolutionary Lineages`.
- Не стоит делать отдельный `domain: phylogenesis`, потому что это не самостоятельная disciplinary optic, а центральный кластер внутри более широкой ветки `Evolutionary Biology`.
- `Ontogenesis` остается поперечной связью, а не родительской веткой, потому что соотношение онтогенеза и филогенеза важно концептуально, но не превращает одну тему в подраздел другой.

## Что не стоит делать прямо сейчас

- Не стоит подчинять `Phylogenesis` ветке `Developmental Biology`.
- Не стоит заранее создавать большой пакет дочерних notes для `Speciation`, `Cladogenesis`, `Common Ancestry`, `Homology` и `Phylogenetic Trees`, пока рядом нет устойчивого корпуса.
- Не стоит создавать отдельный `domain` под `Phylogenesis`.
- Не стоит создавать отдельные тематические template-файлы под biology или evolutionary biology: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── B/
│   └── Biology.md
├── D/
│   └── Developmental Biology.md
├── E/
│   └── Evolutionary Biology.md
├── O/
│   └── Ontogenesis.md
└── P/
    └── Phylogenesis.md
```

## Что уже создано в Inbox

- `[[Biology]]`
- `[[Evolutionary Biology]]`
- `[[Phylogenesis]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: evolutionary-biology`
- [ ] Подтвердить `section: phylogenesis`
- [ ] Решить, когда внутри `Phylogenesis` нужны отдельные дочерние статьи
- [ ] Проверить границы между phylogenesis, ontogenesis и systematics
