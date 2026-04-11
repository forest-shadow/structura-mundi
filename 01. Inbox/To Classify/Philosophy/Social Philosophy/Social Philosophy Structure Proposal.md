---
aliases:
  - Социальная философия Structure Proposal
  - Структура ветки Social Philosophy
note_type: article
area: philosophy
domain: social-philosophy
section:
parent:
status: draft
related:
  - "[[Philosophy]]"
  - "[[Social Philosophy]]"
  - "[[Power and Subjection]]"
  - "[[Servility]]"
tags: []
---

# Social Philosophy Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для новой domain-root ветки `Social Philosophy` внутри `Philosophy`, в которую естественно помещается рассмотрение такого понятия, как `Servility`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: philosophy`
- `domain: social-philosophy` (новое рабочее значение)
- `section:` пусто у domain-root overview `Social Philosophy`

Почему так:

- существующие значения `ancient-philosophy` и `logic` не подходят: `Servility` не является ни историко-философской школой, ни формально-логическим понятием;
- тема требует не одной isolated note, а устойчивой рамки для серии понятий о власти, зависимости, подчинении, свободе и общественных формах господства;
- новое значение `domain: social-philosophy` полезно не только для `Servility`, но и для возможных соседних заметок вроде conformity, domination, obedience, authority и alienation.

## Рекомендуемая иерархия

```text
Philosophy
└── Social Philosophy
    └── Power and Subjection
        └── Servility
```

## Почему структура именно такая

- `Social Philosophy` оправдана как новый domain-root, потому что без нее `Servility` пришлось бы либо оставлять висящим прямо под `Philosophy`, либо искусственно встраивать в `Ancient Philosophy` или `logic`.
- `Power and Subjection` уместно как section-level overview, потому что `Servility` естественно соседствует не с любыми социально-философскими темами вообще, а с понятиями о социальной зависимости, иерархии и адаптации к власти.
- `Servility` пока лучше держать обычной `article`, а не раздувать отдельный локальный overview, пока вокруг него нет устойчивого корпуса дочерних статей.

## Что не стоит создавать заранее

- отдельный `domain` вроде `political-philosophy`, если пока основной корпус вращается вокруг более широкой социальной оптики власти и подчинения, а не вокруг полноценной политико-философской ветки институтов и легитимности;
- отдельные sibling-ветки внутри `social-philosophy` только ради симметрии, пока рядом нет устойчивого корпуса;
- тематические template-файлы под социальную философию: по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

После нормализации в `02. Corpus Mundi` эти заметки должны раскладываться по алфавитному корпусному индексу, а логическая ветка при этом должна собираться через `parent`, а не через физические подпапки.

## Что уже создано в Inbox

- `[[Social Philosophy]]`
- `[[Power and Subjection]]`
- `[[Servility]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: social-philosophy`
- [ ] Подтвердить `section: power-and-subjection`
- [ ] Решить, когда рядом с `Servility` нужны заметки про conformity, domination, authority и obedience
- [ ] Проверить `related`
