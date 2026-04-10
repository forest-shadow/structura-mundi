---
aliases:
  - Платоновская космология Structure Proposal
note_type: article
area: philosophy
domain: ancient-philosophy
section: plato
parent: "[[Plato]]"
status: draft
related:
  - "[[Plato]]"
  - "[[Platonic Cosmology]]"
  - "[[Platonic Cosmos]]"
  - "[[Platonic Demiurge]]"
  - "[[World Soul]]"
tags: []
---

# Platonic Cosmology Structure Proposal

## Краткое определение

This file fixes the minimal hierarchy of notes in which the concept `Platonic Cosmos` can be naturally placed according to `Principia Rerum`.

## Рекомендуемая иерархия

```text
Philosophy
└── Ancient Philosophy
    └── Plato
        └── Platonic Cosmology
            ├── Platonic Cosmos
            ├── Platonic Demiurge
            └── World Soul
```

## Почему структура именно такая

- `Ancient Philosophy` нужен как `domain-root overview`, потому что тема относится не к формальной логике, а к историко-философскому корпусу античности.
- `Plato` лучше держать как `section-level overview`, потому что это устойчивый кластер, внутри которого естественно ожидать не одну, а несколько подветок.
- `Platonic Cosmology` уместна как вложенный `overview`, потому что рядом уже есть несколько тесно связанных понятий: `Platonic Cosmos`, `Platonic Demiurge` и `World Soul`.
- `Platonic Cosmos` должен быть отдельной `article`, потому что это не вся ветка целиком, а один центральный космологический концепт внутри платоновской модели мира.

## Что не стоит создавать заранее

- отдельную заметку `Platonism`, если на текущем этапе нужен не общий корпус всей школы, а именно космологический кластер внутри ветки `Plato`;
- специальные тематические template-файлы под эту ветку, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`;
- слишком ранние отдельные статьи `Chora` и `Timaeus`, если локальный корпус еще не требует такого уровня детализации.

## Предлагаемое физическое размещение после нормализации

If the branch is confirmed and brought to canonical state, the physical placement should follow the alphabetical rule:

```text
02. Corpus Mundi/
├── A/
│   └── Ancient Philosophy.md
├── P/
│   ├── Philosophy.md
│   ├── Plato.md
│   ├── Platonic Cosmology.md
│   ├── Platonic Cosmos.md
│   └── Platonic Demiurge.md
└── W/
    └── World Soul.md
```

The logical branch is assembled through `parent`, not through nested directories.

## Созданные seed-заготовки

- `Philosophy.md`
- `Ancient Philosophy.md`
- `Plato.md`
- `Platonic Cosmology.md`
- `Platonic Cosmos.md`
- `Platonic Demiurge.md`
- `World Soul.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: ancient-philosophy`.
2. Подтвердить `section: plato`.
3. Решить, когда рядом действительно нужны `Chora` и `Timaeus` как отдельные статьи.
4. Проверить, не нужен ли позже более широкий overview `Platonism`.
