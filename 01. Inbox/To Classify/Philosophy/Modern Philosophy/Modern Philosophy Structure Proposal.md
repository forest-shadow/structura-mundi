---
aliases:
  - Modern Philosophy Branch Structure Proposal
  - Структура ветки Modern Philosophy
note_type: article
area: philosophy
domain: modern-philosophy
section:
parent:
status: draft
related:
  - "[[Philosophy]]"
  - "[[Modern Philosophy]]"
  - "[[Hegel Georg Wilhelm Friedrich]]"
tags: []
---

# Modern Philosophy Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для новой domain-root ветки `Modern Philosophy` внутри `Philosophy`, в которую естественно помещается рассмотрение такого понятия, как `Georg Wilhelm Friedrich Hegel`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: philosophy`
- `domain: modern-philosophy`
- `section:` пусто у domain-root overview `Modern Philosophy`

Почему так:

- `Hegel Georg Wilhelm Friedrich` неудобно держать прямо под `Philosophy`, потому что тогда теряется историко-философская рамка новоевропейской мысли;
- существующие домены `ancient-philosophy`, `social-philosophy` и `logic` не подходят: Hegel не является ни античным философом, ни локальным сюжетом социальной философии, ни формально-логической темой;
- новое значение `domain: modern-philosophy` полезно не только для Hegel, но и для будущих веток вроде Kant, Fichte, Schelling, phenomenology и post-Kantian idealism.

## Рекомендуемая иерархия

```text
Philosophy
└── Modern Philosophy
    └── Hegel Georg Wilhelm Friedrich
        ├── Hegel Georg Wilhelm Friedrich Biography and Intellectual Context
        ├── Hegel Georg Wilhelm Friedrich System and Method
        └── Hegel Georg Wilhelm Friedrich Works and Influence
```

## Почему структура именно такая

- `Modern Philosophy` оправдана как новый domain-root, потому что она дает устойчивую рамку для новоевропейских философских систем, не раздувая `Philosophy` в плоский список имен.
- `Hegel Georg Wilhelm Friedrich` уместен как section-level overview, потому что вокруг Hegel естественно собирать не одну заметку, а несколько самостоятельных слоев: биографико-интеллектуальный контекст, устройство системы и корпус работ с влиянием.
- Три дочерние статьи разделяют разные режимы чтения: жизнь и контекст, собственно философскую архитектуру, а затем тексты и последействие.
- Отдельные заметки вроде `Absolute Idealism`, `Hegelian Dialectic` или `Phenomenology of Spirit` лучше не создавать автоматически только ради симметрии. Они понадобятся тогда, когда станут самостоятельными каноническими точками чтения, а не placeholder-именами.

## Что не стоит создавать заранее

- отдельный `domain` вроде `german-idealism`, пока рядом еще нет устойчивого корпуса соседних фигур и понятий;
- отдельный `section`, параллельный `hegel`, только ради будущей симметрии с Kant или Schelling;
- тематические template-файлы под modern philosophy или Hegel, потому что по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

После переноса в `02. Corpus Mundi` заметки должны разойтись по алфавитным директориям:

```text
02. Corpus Mundi/
├── H/
│   └── Hegel Georg Wilhelm Friedrich.md
├── M/
│   └── Modern Philosophy.md
├── P/
│   └── Philosophy.md
└── ...
```

Логическая ветка при этом собирается через `parent`, а не через физические подпапки.

## Созданные seed-заготовки

- `[[Modern Philosophy]]`
- `[[Hegel Georg Wilhelm Friedrich]]`
- `[[Hegel Georg Wilhelm Friedrich Biography and Intellectual Context]]`
- `[[Hegel Georg Wilhelm Friedrich System and Method]]`
- `[[Hegel Georg Wilhelm Friedrich Works and Influence]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `domain: modern-philosophy`
- [ ] Подтвердить `section: hegel`
- [ ] Решить, когда рядом с персональной веткой нужны отдельные статьи `Absolute Idealism`, `Hegelian Dialectic` и `Phenomenology of Spirit`
- [ ] Проверить `related`
