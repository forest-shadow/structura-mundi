# JavaScript Prototype System Structure Proposal

## Назначение

Этот файл фиксирует подветку `JavaScript Prototype System` внутри более общей темы `JavaScript` по правилам `Principia Rerum`.

Для этой ветки подходит уже подтвержденная словарная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: javascript`

## Рекомендуемая иерархия

```text
JavaScript (overview)
└── JavaScript Prototype System (overview)
    ├── JavaScript Prototype Internal Slot (article)
    ├── Proto Accessor (article)
    ├── JavaScript prototype Property (article)
    └── Prototype Chain (article)
```

## Почему структура именно такая

- `JavaScript Prototype System` является естественным `overview`, который собирает под одной крышей часто путаемые понятия.
- `JavaScript Prototype Internal Slot`, `Proto Accessor` и `JavaScript prototype Property` нужно держать как отдельные `article`, потому что они связаны, но не тождественны.
- `Prototype Chain` тоже лучше выделять в самостоятельную статью: это не просто свойство или слот, а модель разрешения свойств и наследования.
- Дополнительный уровень вложенности пока не нужен.

## Что пока не нужно создавать

- `JavaScript Object Model` как более широкий `overview`, если ветка пока не вышла за пределы prototype system;
- `Classes and Prototypes` как отдельную подветку;
- отдельные статьи для `Object.create`, `Object.getPrototypeOf` и `Object.setPrototypeOf`, если пока речь идёт о базовой концептуальной карте.

## Следующий шаг перед переносом в Corpus Mundi

1. Синхронизировать именование узлов с уже существующими corpus-статьями.
2. После этого перевести заметки из `seed` в содержательные черновики и наполнить материалом.
