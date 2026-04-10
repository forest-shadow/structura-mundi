# JavaScript Structure Proposal

## Назначение

Этот файл фиксирует общую иерархию заметок для темы `JavaScript` по правилам `Principia Rerum`.

Ветка собирает под одним корнем уже существующие JavaScript-подветки, чтобы заметки про scope, closure и prototype system не существовали как отдельные полукорни без общей обзорной рамки.

Для этой ветки подходит уже подтвержденная словарная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: javascript`

## Рекомендуемая иерархия

```text
JavaScript (overview)
├── JavaScript Prototype System (overview)
│   ├── JavaScript Prototype Internal Slot (article)
│   ├── Proto Accessor (article)
│   ├── JavaScript prototype Property (article)
│   └── Prototype Chain (article)
├── JavaScript Property Model (overview)
│   ├── JavaScript Property Descriptor (article)
│   ├── JavaScript Data Property (article)
│   └── JavaScript Accessor Property (article)
└── JavaScript Scope Model (overview)
    ├── Lexical Scope (article)
    ├── Scope Chain (article)
    └── JavaScript Closure (article)
```

## Почему структура именно такая

- `JavaScript` нужен как корневой `overview`, потому что в `Inbox` уже есть несколько устойчивых подветок про один и тот же язык.
- `JavaScript Prototype System` и `JavaScript Scope Model` оправданы как отдельные `overview`, потому что каждая из этих тем уже образует собственный плотный кластер статей.
- `JavaScript Property Model` оправдан как отдельный, но узкий `overview`, потому что `Accessor Property` относится не только к прототипам, а к общей модели свойств объекта и descriptor-level семантике.
- Подветки остаются минимально вложенными: `root overview -> sub-overview -> article`.
- Более широкие узлы вроде `JavaScript Runtime Model` или `JavaScript Object Model` пока не нужны без дополнительного корпуса; `JavaScript Property Model` оставляет ветку уже и точнее.

## Что не стоит создавать заранее

- промежуточные overview-слои только ради симметрии;
- отдельные статьи на слишком мелкие аспекты closure и prototype semantics без устойчивого корпуса;
- отдельную корневую ветку только для `functions`, если пока материал естественно встраивается в scope model.
- отдельный тематический template-файл под JavaScript object/property notes, потому что по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

Если заметки будут доведены до канонического состояния, их физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── J/
│   ├── JavaScript.md
│   ├── JavaScript Accessor Property.md
│   ├── JavaScript Closure.md
│   ├── JavaScript Data Property.md
│   ├── JavaScript Property Descriptor.md
│   ├── JavaScript Property Model.md
│   ├── JavaScript Prototype Internal Slot.md
│   ├── JavaScript Prototype System.md
│   ├── JavaScript Scope Model.md
│   └── JavaScript prototype Property.md
├── L/
│   └── Lexical Scope.md
├── P/
│   ├── Proto Accessor.md
│   └── Prototype Chain.md
└── S/
    └── Scope Chain.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `JavaScript.md`
- `JavaScript Prototype System.md`
- `JavaScript Prototype Internal Slot.md`
- `JavaScript prototype Property.md`
- `JavaScript Property Model.md`
- `JavaScript Property Descriptor.md`
- `JavaScript Data Property.md`
- `JavaScript Accessor Property.md`
- `JavaScript Scope Model.md`
- `Lexical Scope.md`
- `Scope Chain.md`
- `JavaScript Closure.md`
- `Proto Accessor.md`
- `Prototype Chain.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Развести границы между scope model, execution context и function internals.
2. Синхронизировать именование prototype-узлов с уже существующими corpus-статьями.
3. Развести границы между property model, prototype system и возможной будущей object model.
4. После этого наполнять заметки содержанием и повышать зрелость.
