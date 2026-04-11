---
aliases:
  - Tibetan Buddhism Structure Proposal
  - Структура ветки Tibetan Buddhism
note_type: article
area: religion
domain: religious-studies
section: tibetan-buddhism
parent:
status: draft
related:
  - "[[Religion]]"
  - "[[Religious Studies]]"
  - "[[Tibetan Buddhism]]"
  - "[[Seed Syllables]]"
  - "[[A (Tibetan Buddhism)]]"
tags: []
---

# Tibetan Buddhism Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Tibetan Buddhism`, в которую естественно помещается рассмотрение такого понятия, как слог `A` в тибетском буддизме, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: religion`
- `domain: religious-studies` (переиспользуем уже существующее значение)
- `section: tibetan-buddhism` для обзорной ветки традиции
- `section: seed-syllables` для локального кластера сакральных слогов внутри этой ветки

Почему так:

- тема относится не к мифологическому корпусу, а к религиоведческому рассмотрению традиции, практики и символики;
- для одной локальной ветки преждевременно вводить новый `domain` вроде `buddhist-studies`;
- `Tibetan Buddhism` уже представляет собой достаточно устойчивую и содержательно самостоятельную традицию, чтобы быть section-level узлом внутри `religious-studies`;
- `Seed Syllables` теперь вводится как отдельный sub-overview, потому что пользователь явно хочет собирать эту символическую подветку как самостоятельный локальный кластер.

## Канонические имена

- area-level root: `Religion`
- domain-root overview: `Religious Studies`
- section-level overview: `Tibetan Buddhism`
- sub-overview: `Seed Syllables`
- article: `A (Tibetan Buddhism)`

Уточнение в имени `A (Tibetan Buddhism)` здесь оправдано, потому что краткое имя `A` слишком неоднозначно и без контекста не различает тему.

## Рекомендуемая иерархия

```text
Religion
└── Religious Studies
    └── Tibetan Buddhism
        └── Seed Syllables
            └── A (Tibetan Buddhism)
```

## Почему структура именно такая

- `Religion` уже существует как area-level overview, поэтому новый верхний уровень создавать не нужно.
- `Religious Studies` уже существует как domain-root overview и естественно принимает ветку о конкретной религиозной традиции.
- `Tibetan Buddhism` оправдан как section-level overview, потому что это большая и устойчивая традиция, внутри которой могут появляться собственные статьи о символах, практиках, школах и доктринальных мотивах.
- `Seed Syllables` теперь выступает как допустимый `sub-overview`, который собирает не всю традицию, а один локальный смысловой кластер внутри нее.
- `A (Tibetan Buddhism)` остается обычной `article`, но теперь подчиняется более точному промежуточному узлу.

## Что не стоит делать прямо сейчас

- Не стоит помещать `A (Tibetan Buddhism)` напрямую под `Religion`, потому что тогда теряется дисциплинарная и традиционная рамка.
- Не стоит преждевременно вводить `Buddhist Studies` как отдельный `domain`, пока в vault нет устойчивой серии соседних буддийских веток.
- Не стоит создавать отдельные тематические template-файлы под тибетский буддизм: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`, развернутых в конкретные заметки ветки.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── A (Tibetan Buddhism).md
├── R/
│   └── Religious Studies.md
├── S/
│   └── Seed Syllables.md
└── T/
    └── Tibetan Buddhism.md
```

## Что уже создано в Inbox

- `[[Tibetan Buddhism]]`
- `[[Seed Syllables]]`
- `[[A (Tibetan Buddhism)]]`

Эти заметки созданы как канонические заготовки на базе разрешенных шаблонов `overview/article`, без введения новых domain-specific templates.

## Что стоит раскрыть дальше

- [ ] Решить, какие еще статьи должны войти в `Seed Syllables`
- [ ] Подтвердить `section: seed-syllables`, если подветка получит продолжение
- [ ] Проверить `related`
