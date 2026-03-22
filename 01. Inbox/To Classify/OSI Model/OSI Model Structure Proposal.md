# OSI Model Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `OSI Model` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: networking` (предлагаемое новое значение)
- `section: network-models` (предлагаемое новое значение)

`OSI Model` оправдан как отдельный `overview`, потому что это не одна изолированная статья, а устойчивая рамка для семи взаимосвязанных уровней сетевой архитектуры. При этом ветку не нужно перегружать лишними подветками: на текущем этапе достаточно одного обзорного узла и плоского набора дочерних статей по слоям.

## Рекомендуемая иерархия

```text
OSI Model (overview)
├── Physical Layer (article)
├── Data Link Layer (article)
├── Network Layer (article)
├── Transport Layer (article)
├── Session Layer (article)
├── Presentation Layer (article)
└── Application Layer (article)
```

## Почему структура именно такая

- `OSI Model` служит обзорной картой для всей модели и позволяет объяснить назначение каждого слоя в общей архитектуре.
- Каждый слой является самостоятельным объектом знания и заслуживает собственной канонической статьи.
- Дополнительные подветки вроде `Encapsulation`, `Protocol Data Units` или `Layer Interaction` пока не нужны: их можно раскрывать как разделы внутри `OSI Model` или внутри статей по слоям.
- Ветка остаётся плоской и предсказуемой, что соответствует правилу минимальной вложенности.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `OSI vs TCP/IP`, если это будет только сравнительный раздел внутри `OSI Model`;
- `Encapsulation in OSI Model`, если это пока не тянет на самостоятельную статью;
- `Layer 2`, `Layer 3`, `Layer 4` как дубли канонических имен слоёв;
- отдельные заметки на каждый пример протокола без сформировавшейся ветки.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   └── Application Layer.md
├── D/
│   └── Data Link Layer.md
├── N/
│   └── Network Layer.md
├── O/
│   └── OSI Model.md
├── P/
│   ├── Physical Layer.md
│   └── Presentation Layer.md
├── S/
│   └── Session Layer.md
└── T/
    └── Transport Layer.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `OSI Model.md`
- `Physical Layer.md`
- `Data Link Layer.md`
- `Network Layer.md`
- `Transport Layer.md`
- `Session Layer.md`
- `Presentation Layer.md`
- `Application Layer.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: networking`.
2. Подтвердить `section: network-models`.
3. Наполнить `OSI Model` так, чтобы различие между слоями было кратко и чётко видно уже из overview.
4. Позже решить, нужен ли отдельный соседний `overview` для `TCP/IP Model`.
