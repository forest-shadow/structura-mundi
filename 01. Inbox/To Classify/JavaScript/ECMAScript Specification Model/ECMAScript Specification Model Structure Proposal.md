---
aliases:
  - JavaScript Specification Model Structure Proposal
  - ECMAScript Spec Notation Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent:
status: seed
related:
  - "[[JavaScript]]"
  - "[[ECMAScript Specification Model]]"
  - "[[ECMAScript Internal Bracket Notation]]"
  - "[[ECMAScript Internal Slot]]"
  - "[[ECMAScript Internal Method]]"
  - "[[ECMAScript Abstract Operation]]"
  - "[[JavaScript Prototype Internal Slot]]"
tags: []
---

# ECMAScript Specification Model Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для подветки `ECMAScript Specification Model`, в которую естественно помещается рассмотрение такого понятия, как `JavaScript Internal Brackets Notation`, по правилам `Principia Rerum`.

Для этой ветки подходит уже подтвержденная словарная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: javascript`

Новый `domain` или `section` не нужен: речь идет о формальной спецификационной оптике внутри уже существующей JavaScript-ветки.

## Рекомендуемая иерархия

```text
JavaScript (overview)
└── ECMAScript Specification Model (overview)
    ├── ECMAScript Internal Bracket Notation (article)
    ├── ECMAScript Internal Slot (article)
    ├── ECMAScript Internal Method (article)
    └── ECMAScript Abstract Operation (article)
```

Поперечные связи:

```text
ECMAScript Internal Bracket Notation ↔ JavaScript Prototype Internal Slot
ECMAScript Internal Slot ↔ JavaScript Prototype Internal Slot
ECMAScript Internal Method ↔ JavaScript Property Model
ECMAScript Abstract Operation ↔ JavaScript Prototype System
```

## Почему структура именно такая

- `ECMAScript Specification Model` оправдан как узкий вложенный `overview`, потому что `[[...]]`-нотация встречается не только в `[[Prototype]]`, но и в internal methods, property attributes, specification records и abstract operations.
- `ECMAScript Internal Bracket Notation` должна быть отдельной `article`, потому что это нотационная рамка чтения спецификации, а не один конкретный слот или метод.
- `ECMAScript Internal Slot` и `ECMAScript Internal Method` нужно держать как соседние `article`: обе категории записываются через двойные квадратные скобки, но первая описывает внутреннее состояние, а вторая - алгоритмическое поведение объекта.
- `ECMAScript Abstract Operation` стоит держать рядом, потому что abstract operations вроде `OrdinaryObjectCreate` или `GetPrototypeFromConstructor` часто вызывают или объясняют internal slots/methods, но не являются тем же самым типом сущности.
- `JavaScript Prototype Internal Slot` остается в ветке `JavaScript Prototype System`, потому что это частный прототипный слот `[[Prototype]]`; общая статья `ECMAScript Internal Slot` связывается с ним через `related`, а не заменяет его.

## Что не стоит создавать заранее

- отдельный `JavaScript Object Model`, пока нет устойчивого корпуса про ordinary objects, exotic objects, realms и agents;
- отдельные статьи про каждый internal method (`[[Get]]`, `[[Set]]`, `[[DefineOwnProperty]]`) без плотного корпуса;
- отдельные статьи про каждый property attribute (`[[Value]]`, `[[Writable]]`, `[[Get]]`, `[[Set]]`) без необходимости;
- специальные тематические template-файлы под ECMAScript specification notes, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
01. Inbox/To Classify/JavaScript/
└── ECMAScript Specification Model/
    ├── ECMAScript Specification Model Structure Proposal.md
    ├── ECMAScript Specification Model.md
    ├── ECMAScript Internal Bracket Notation.md
    ├── ECMAScript Internal Slot.md
    ├── ECMAScript Internal Method.md
    └── ECMAScript Abstract Operation.md
```

## Предлагаемое физическое размещение после нормализации

Если ветка будет доведена до канонического состояния, ее физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── E/
    ├── ECMAScript Abstract Operation.md
    ├── ECMAScript Internal Bracket Notation.md
    ├── ECMAScript Internal Method.md
    ├── ECMAScript Internal Slot.md
    └── ECMAScript Specification Model.md
```

Логическая ветка при этом все равно собирается через `parent`, `related` и `section`, а не через физическое соседство файлов.

## Созданные seed-заготовки

- `[[ECMAScript Specification Model]]`
- `[[ECMAScript Internal Bracket Notation]]`
- `[[ECMAScript Internal Slot]]`
- `[[ECMAScript Internal Method]]`
- `[[ECMAScript Abstract Operation]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границы между `ECMAScript Specification Model`, `JavaScript Property Model` и `JavaScript Prototype System`.
2. Наполнить `ECMAScript Internal Bracket Notation` примерами `[[Prototype]]`, `[[Get]]`, `[[Value]]` и `[[Type]]`.
3. Проверить, нужен ли позднее отдельный article про `ECMAScript Record Type`.
4. После наполнения поднять статус ключевых заметок с `seed` до `draft`.
