# React Hooks Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `React Hooks` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: frontend-engineering` (предлагаемое новое значение)
- `section: react-hooks` (предлагаемое новое значение)

До фиксации этих значений в `Controlled Vocabulary` ветку не стоит считать готовой к переносу в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
React Hooks (overview)
├── Rules of Hooks (article)
├── useState (article)
├── useEffect (article)
├── useReducer (article)
├── useContext (article)
├── useRef (article)
└── Custom Hooks (article)
```

## Почему структура именно такая

- `React Hooks` является естественной канонической обзорной точкой входа для всей ветки.
- На стартовом этапе вложенные `overview` не нужны: базовые темы уже хорошо ложатся в плоский набор `article`.
- `Rules of Hooks` важно держать рядом с конкретными API-хуками, потому что это не просто вспомогательная заметка, а нормативный каркас всей темы.
- `Custom Hooks` заслуживает отдельной статьи, потому что это самостоятельный концепт, а не просто список встроенных API.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Core Hooks` как промежуточный слой только ради группировки;
- `Effect Hooks`, `State Hooks`, `Performance Hooks`, если по ним еще нет отдельного плотного корпуса;
- отдельные заметки для `useMemo`, `useCallback`, `useLayoutEffect`, `useTransition`, если ветка пока не разрослась до этого уровня;
- отдельный обзорный узел `React`, если сейчас строится именно ветка по hooks.

Эти темы можно добавить позже, если ветка реально вырастет.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, их естественное размещение:

```text
02. Corpus Mundi/
└── R/
    ├── React Hooks.md
    ├── Rules of Hooks.md
    ├── useState.md
    ├── useEffect.md
    ├── useReducer.md
    ├── useContext.md
    ├── useRef.md
    └── Custom Hooks.md
```

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
3. Решить, нужен ли позже более широкий обзорный узел для `React`.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
