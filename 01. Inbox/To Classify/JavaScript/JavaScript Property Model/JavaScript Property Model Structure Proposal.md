---
aliases:
  - JavaScript Object Property Model Structure Proposal
  - JavaScript Properties Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: javascript
parent:
status: seed
related:
  - "[[JavaScript]]"
  - "[[JavaScript Property Model]]"
  - "[[JavaScript Accessor Property]]"
  - "[[JavaScript Prototype System]]"
tags: []
---

# JavaScript Property Model Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для подветки `JavaScript Property Model`, в которую естественно помещается рассмотрение такого понятия, как `JavaScript Accessor Property`, по правилам `Principia Rerum`.

Для этой ветки подходит уже подтвержденная словарная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: javascript`

Новый `domain` или `section` не нужен: речь идет не о самостоятельной дисциплине, а о внутренней модели свойств языка JavaScript внутри уже существующей JS-ветки.

## Рекомендуемая иерархия

```text
JavaScript (overview)
└── JavaScript Property Model (overview)
    ├── JavaScript Property Descriptor (article)
    ├── JavaScript Data Property (article)
    └── JavaScript Accessor Property (article)
```

## Почему структура именно такая

- `JavaScript Property Model` оправдан как вложенный `overview`, потому что `Accessor Property` не является частным случаем только прототипной системы. Это элемент общей модели свойств объекта, который связан с descriptors, data properties, assignment semantics и prototype lookup.
- `JavaScript Property Descriptor` лучше держать обычной `article`, а не отдельным `overview`, потому что на текущем этапе оно объясняет форму описания свойств и связывает две основные разновидности свойств, но не требует собственного глубинного дерева.
- `JavaScript Data Property` и `JavaScript Accessor Property` должны быть соседними `article`: они являются двумя фундаментальными категориями свойств и хорошо объясняются через контраст.
- `Proto Accessor` остается в ветке `JavaScript Prototype System`, потому что `__proto__` - это конкретный legacy-accessor для работы с прототипом. Его нужно связывать с `JavaScript Accessor Property` через `related`, а не делать родителем или дочерней статьей.
- Более широкий `JavaScript Object Model` пока не нужен: новая подветка покрывает только модель свойств, а не всю объектную модель языка.

## Что не стоит создавать заранее

- отдельный `overview` `JavaScript Object Model`, пока нет устойчивого корпуса про ordinary objects, exotic objects, internal methods и realms;
- отдельный `overview` `JavaScript Property Descriptor Model`, если пока достаточно одной статьи `JavaScript Property Descriptor`;
- отдельные заметки под каждое поле descriptor (`value`, `writable`, `get`, `set`, `enumerable`, `configurable`), пока они не имеют самостоятельного корпуса;
- специальные тематические template-файлы под JavaScript property notes, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
01. Inbox/To Classify/JavaScript/
└── JavaScript Property Model/
    ├── JavaScript Property Model Structure Proposal.md
    ├── JavaScript Property Model.md
    ├── JavaScript Property Descriptor.md
    ├── JavaScript Data Property.md
    └── JavaScript Accessor Property.md
```

## Предлагаемое физическое размещение после нормализации

Если ветка будет доведена до канонического состояния, ее физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── J/
    ├── JavaScript Accessor Property.md
    ├── JavaScript Data Property.md
    ├── JavaScript Property Descriptor.md
    └── JavaScript Property Model.md
```

Логическая ветка при этом все равно собирается через `parent`, а не через физическое соседство файлов.

## Созданные seed-заготовки

- `[[JavaScript Property Model]]`
- `[[JavaScript Property Descriptor]]`
- `[[JavaScript Data Property]]`
- `[[JavaScript Accessor Property]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границы между `JavaScript Property Model`, `JavaScript Prototype System` и возможной будущей веткой `JavaScript Object Model`.
2. Наполнить `JavaScript Accessor Property` примерами getter/setter-свойств и связать ее с `[[Proto Accessor]]`.
3. Проверить, нужен ли позднее отдельный article `JavaScript Own Property`, если появится больше материала про own/inherited property distinction.
4. После наполнения поднять статус ключевых заметок с `seed` до `draft`.
