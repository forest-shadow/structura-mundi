---
aliases:
  - Parapsychology Structure Proposal
  - Структура ветки Parapsychology
note_type: article
area: religion
domain: religious-studies
section: parapsychology
parent:
status: draft
related:
  - "[[Religion]]"
  - "[[Religious Studies]]"
  - "[[Parapsychology]]"
  - "[[Psychotronics]]"
tags: []
---

# Parapsychology Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Parapsychology`, в которую естественно помещается рассмотрение такого понятия, как `Psychotronics`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: religion`
- `domain: religious-studies` (переиспользуем уже существующее значение)
- `section: parapsychology` (новый локальный кластер внутри `religious-studies`)

Почему так:

- в рамках текущего словаря `area/domain` в vault нет отдельной устойчивой области вроде `psychology`, `history-of-science` или `esotericism`, куда эту тему можно было бы встроить естественнее;
- `Psychotronics` исторически и понятийно ближе всего к корпусу тем о `parapsychology`, psi-феноменах, психической энергии, экстрасенсорике и пограничных оккультно-научных моделях, а не к мифологическим сюжетам;
- новый `domain` под одну ветку вводить преждевременно: по `Principia Rerum` здесь разумнее использовать уже существующий `religious-studies` как аналитическую рамку для спорных и пограничных представлений о сверхобычном опыте и скрытых силах;
- `section: parapsychology` достаточно узок, чтобы собрать рядом будущие заметки вроде `Telepathy`, `Psychokinesis`, `ESP`, `Psychoenergetics` или `Remote Viewing`, если такой корпус действительно появится.

## Канонические имена

- area-level root: `Religion`
- domain-root overview: `Religious Studies`
- section-level overview: `Parapsychology`
- article: `Psychotronics`

`Парапсихология` и `Психотроника` лучше хранить в `aliases`, а не делать отдельными русскоязычными дублями.

## Рекомендуемая иерархия

```text
Religion
└── Religious Studies
    └── Parapsychology
        └── Psychotronics
```

## Почему структура именно такая

- `Religion` уже существует как area-level overview, поэтому новый верхний уровень не нужен.
- `Religious Studies` уже существует как domain-root overview и лучше всего принимает темы, которые нужно рассматривать не как персонажей мифа, а как исследовательские и интерпретативные режимы чтения религиозного, мистического и сверхобычного.
- `Parapsychology` здесь уместен как section-level overview, потому что `Psychotronics` не выглядит одиночным изолированным термином: вокруг него естественно ожидается соседний корпус понятий о psi-феноменах и соответствующих исследовательских программах.
- `Psychotronics` лучше оставить обычной `article`, а не делать из нее overview, потому что на текущем этапе это конкретный термин и историко-концептуальная рамка внутри более широкой парапсихологической ветки.

## Что не стоит делать прямо сейчас

- не стоит помещать `Psychotronics` напрямую под `Religion`, потому что тогда теряется дисциплинарная рамка;
- не стоит относить `Psychotronics` к `Mythology`, потому что речь идет не о мифологическом корпусе, а о попытках описывать и исследовать психические или сверхобычные феномены;
- не стоит преждевременно вводить новый `domain` вроде `parapsychology`, `esotericism` или `occult-studies`, пока рядом нет устойчивой серии sibling-веток;
- не стоит создавать отдельные тематические template-файлы под `Psychotronics` или `Parapsychology`: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`, развернутых в конкретные заметки ветки.

## Предлагаемое физическое размещение в Inbox

```text
01. Inbox/
└── To Classify/
    └── Religion/
        └── Religious Studies/
            └── Parapsychology/
                ├── Parapsychology Structure Proposal.md
                ├── Parapsychology.md
                └── Psychotronics.md
```

## Что уже создано в этой ветке

- `[[Parapsychology]]`
- `[[Psychotronics]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Psychotronics` нужны отдельные статьи про `Telepathy`, `Psychokinesis`, `ESP` и `Psychoenergetics`
- [ ] Проверить, не потребует ли ветка со временем более точного переноса из `religious-studies` в отдельный `domain`, если в vault появится устойчивый корпус по истории оккультной науки или паранаучных дисциплин
- [ ] Подтвердить `section: parapsychology`
- [ ] Проверить `related`
