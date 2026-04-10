---
aliases:
  - Theory of Ideas Structure Proposal
note_type: article
area: philosophy
domain: ancient-philosophy
section: plato
parent: "[[Plato]]"
status: draft
related:
  - "[[Plato]]"
  - "[[Theory of Forms]]"
  - "[[Eidos]]"
  - "[[Platonic Form]]"
  - "[[Participation]]"
  - "[[The Good]]"
  - "[[Recollection]]"
tags: []
---

# Theory of Forms Structure Proposal

## Краткое определение

This file fixes the minimal hierarchy of notes in which the concept `Eidos` can be naturally placed according to `Principia Rerum`.

## Рекомендуемая иерархия

```text
Philosophy
└── Ancient Philosophy
    └── Plato
        ├── Platonic Cosmology
        └── Theory of Forms
            ├── Eidos
            ├── Platonic Form
            ├── Participation
            ├── The Good
            └── Recollection
```

## Почему структура именно такая

- `Eidos` лучше не подвешивать напрямую под `Plato`, потому что тогда теряется локальный философский контекст, в котором понятие связано с формами, идеями и participation-relation.
- `Theory of Forms` уместна как вложенный `overview`, потому что это устойчивый платоновский кластер, а не одиночный термин.
- `Eidos` должен быть отдельной `article`, потому что это конкретный концепт и терминологический узел внутри более широкой ветки `Theory of Forms`.
- `Platonic Form` уместен как sibling-статья рядом с `Eidos`, потому что он удерживает не только термин, но и содержательное metaphysical описание form as such.
- `Participation` уместен как sibling-статья, потому что без него ветка про forms быстро становится слишком словарной и теряет один из главных способов связи между forms и чувственными вещами.
- `The Good` и `Recollection` теперь уместны внутри той же ветки, потому что кластер уже перестал быть слишком разреженным и получил устойчивый metaphysical and epistemic объем.

## Что не стоит создавать заранее

- отдельную заметку `Platonism`, если она будет дублировать уже собираемую ветку `Plato`;
- отдельную заметку `Dialectic`, если рядом еще нет устойчивого корпуса для собственной подветки;
- специальные тематические template-файлы под эту ветку, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

If the branch is confirmed and brought to canonical state, the physical placement should follow the alphabetical rule:

```text
02. Corpus Mundi/
├── A/
│   └── Ancient Philosophy.md
├── E/
│   └── Eidos.md
├── P/
│   ├── Philosophy.md
│   ├── Plato.md
│   ├── Platonic Form.md
│   └── Participation.md
├── R/
│   └── Recollection.md
└── T/
    ├── Theory of Forms.md
    └── The Good.md
```

The logical branch is assembled through `parent`, not through nested directories.

## Созданные seed-заготовки

- `Theory of Forms.md`
- `Eidos.md`
- `Platonic Form.md`
- `Participation.md`
- `The Good.md`
- `Recollection.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить, остается ли `Eidos` каноническим именем, а `Form` и `Idea` работают только как `aliases` или `related`.
2. Проверить, как разводить `Eidos` и `Platonic Form` без дублирования.
3. Решить, когда `The Good` потребует собственную подветку.
4. Проверить `related`.
