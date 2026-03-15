# React Hooks Structure Proposal

## Назначение

Этот файл фиксирует hook-подветку внутри более широкой темы `React` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: frontend-engineering` (предлагаемое новое значение)
- `section: react-hooks` (предлагаемое новое значение)

До фиксации этих значений в `Controlled Vocabulary` ветку не стоит считать готовой к переносу в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
React (overview)
└── React Hooks (overview)
    ├── Rules of Hooks (article)
    ├── useState (article)
    ├── useEffect (article)
    ├── useReducer (article)
    ├── useContext (article)
    ├── useRef (article)
    └── Custom Hooks (article)
```

## Почему структура именно такая

- `React Hooks` является естественной обзорной точкой входа именно для hook-подветки.
- Внутри более широкой React-ветки он оправдан как один допустимый вложенный `overview`, потому что уже имеет собственный устойчивый набор дочерних статей.
- `Rules of Hooks` важно держать рядом с конкретными API-хуками, потому что это не просто вспомогательная заметка, а нормативный каркас всей темы.
- `Custom Hooks` заслуживает отдельной статьи, потому что это самостоятельный концепт, а не просто список встроенных API.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Core Hooks` как промежуточный слой только ради группировки;
- `Effect Hooks`, `State Hooks`, `Performance Hooks`, если по ним еще нет отдельного плотного корпуса;
- отдельные заметки для `useMemo`, `useCallback`, `useLayoutEffect`, `useTransition`, если ветка пока не разрослась до этого уровня;
- дополнительные overview-уровни внутри самой hook-ветки.

Эти темы можно добавить позже, если ветка реально вырастет.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, их физическое размещение внутри React-ветки должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── C/
│   └── Custom Hooks.md
├── R/
│   ├── React.md
│   ├── React Hooks.md
│   └── Rules of Hooks.md
└── U/
    ├── useState.md
    ├── useEffect.md
    ├── useReducer.md
    ├── useContext.md
    └── useRef.md
```

`React Hooks` остаётся логическим `sub-overview`, даже если дочерние статьи физически лежат в других буквенных папках.

Локальные вложения при необходимости:

```text
02. Corpus Mundi/R/_resources/React Hooks/
```

## Созданные черновые заметки

- `React Hooks.md`
- `Rules of Hooks.md`
- `useState.md`
- `useEffect.md`
- `useReducer.md`
- `useContext.md`
- `useRef.md`
- `Custom Hooks.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: frontend-engineering`.
2. Подтвердить `section: react-hooks`.
3. Синхронизировать hook-подветку с общей архитектурой `React`.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
