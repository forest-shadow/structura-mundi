# TCP IP Model Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `TCP/IP Model` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: networking` (предлагаемое новое значение)
- `section: network-models` (предлагаемое новое значение)

`TCP/IP Model` оправдан как отдельный `overview`, потому что это устойчивая альтернативная сетeвая модель со своим составом уровней и собственной инженерной значимостью.

Из-за уже существующей ветки `OSI Model` здесь важно избегать двусмысленных имён. Поэтому внутри TCP/IP-подветки используются согласованные уточнённые канонические имена:

- `TCP/IP Link Layer`
- `TCP/IP Internet Layer`
- `TCP/IP Transport Layer`
- `TCP/IP Application Layer`

Это лучше, чем плодить конфликтующие канонические заметки `Transport Layer` и `Application Layer`.

## Рекомендуемая иерархия

```text
TCP/IP Model (overview)
├── TCP/IP Link Layer (article)
├── TCP/IP Internet Layer (article)
├── TCP/IP Transport Layer (article)
└── TCP/IP Application Layer (article)
```

## Почему структура именно такая

- `TCP/IP Model` служит обзорной рамкой для практической модели сетевого стека.
- Каждый слой является самостоятельным объектом знания и заслуживает собственной канонической статьи.
- Симметричное именование всех слоёв внутри ветки делает её более цельной и уменьшает вероятность путаницы.
- Более мелкие темы вроде `Encapsulation`, `Sockets`, `TCP vs UDP`, `TCP/IP vs OSI` пока лучше раскрывать как разделы внутри `TCP/IP Model` или как будущие отдельные ветки, если накопится корпус.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `TCP/IP vs OSI`, если это пока только сравнительный раздел;
- `Layer 4`, `Layer 7` и прочие числовые дубли;
- отдельные статьи на каждый протокол ради примеров слоя;
- промежуточный `Networking Models` overview только ради симметрии между `OSI Model` и `TCP/IP Model`.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── T/
    ├── TCP IP Model.md
    ├── TCP IP Link Layer.md
    ├── TCP IP Internet Layer.md
    ├── TCP IP Transport Layer.md
    └── TCP IP Application Layer.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `TCP IP Model.md`
- `TCP IP Link Layer.md`
- `TCP IP Internet Layer.md`
- `TCP IP Transport Layer.md`
- `TCP IP Application Layer.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: networking`.
2. Подтвердить `section: network-models`.
3. Наполнить `TCP/IP Model` так, чтобы различие между слоями и отличие от `OSI Model` было кратко видно уже из overview.
4. Позже решить, нужен ли отдельный сравнительный `article` про `OSI Model` и `TCP/IP Model`.
