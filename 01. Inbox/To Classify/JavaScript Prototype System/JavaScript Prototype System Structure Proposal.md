# JavaScript Prototype System Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `JavaScript __proto__`, `[[Prototype]]` и связанных понятий по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее предлагаются новые значения словаря:

- `area: computer-science`
- `domain: programming-languages` (предлагаемое новое значение)
- `section: javascript` (предлагаемое новое значение)

`domain` здесь нужен не ради одной заметки, а как будущая общая оптика для тем о языках программирования. `section: javascript` тоже может быть полезен не только для прототипов, но и для других устойчивых заметок о самом языке.

## Рекомендуемая иерархия

```text
JavaScript Prototype System (overview)
├── Internal Prototype Slot (article)
├── Proto Accessor (article)
├── Prototype Property (article)
└── Prototype Chain (article)
```

## Почему структура именно такая

- `JavaScript Prototype System` является естественным `overview`, который собирает под одной крышей часто путаемые понятия.
- `Internal Prototype Slot`, `Proto Accessor` и `Prototype Property` нужно держать как отдельные `article`, потому что они связаны, но не тождественны.
- `Prototype Chain` тоже лучше выделять в самостоятельную статью: это не просто свойство или слот, а модель разрешения свойств и наследования.
- Дополнительный уровень вложенности пока не нужен. Тема достаточно хорошо укладывается в плоскую ветку под одним `overview`.

## Важное решение по каноническим именам

Сырые обозначения спецификации и API не стоит делать каноническими именами файлов:

- `[[Prototype]]` лучше оформить как alias к `Internal Prototype Slot`;
- `__proto__` лучше оформить как alias к `Proto Accessor`;
- `prototype` лучше оформить как alias к `Prototype Property`.

Это помогает:

- не ломать читаемость и именование файлов;
- не создавать конфликт с wiki-синтаксисом Obsidian;
- сохранять совместимость с правилом физического хранения по первой букве канонического имени.

## Что пока не нужно создавать

Пока не стоит заранее заводить отдельные узлы:

- `JavaScript Object Model` как более широкий `overview`, если ветка пока не вышла за пределы prototype-системы;
- `Classes and Prototypes` как отдельную подветку;
- отдельные статьи для `Object.create`, `Object.getPrototypeOf` и `Object.setPrototypeOf`, если пока речь идет о базовой концептуальной карте;
- отдельный `overview` для inheritance, если он пока полностью покрывается текущей веткой.

## Предлагаемое физическое размещение после нормализации

Если `domain` и `section` будут утверждены, а заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── I/
│   └── Internal Prototype Slot.md
├── J/
│   └── JavaScript Prototype System.md
└── P/
    ├── Proto Accessor.md
    ├── Prototype Chain.md
    └── Prototype Property.md
```

Логическая иерархия при этом задается через `parent`, `related` и ссылки, а не через физическую близость файлов.

## Созданные черновые заметки

- `JavaScript Prototype System.md`
- `Internal Prototype Slot.md`
- `Proto Accessor.md`
- `Prototype Property.md`
- `Prototype Chain.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: programming-languages`.
2. Подтвердить `section: javascript`.
3. Решить, нужна ли затем более широкая родительская ветка `JavaScript Object Model`.
4. После этого перевести заметки из `seed` в содержательные черновики и наполнить их материалом.
