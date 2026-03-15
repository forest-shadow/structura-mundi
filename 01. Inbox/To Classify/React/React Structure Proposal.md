# React Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `React` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: frontend-engineering` (предлагаемое новое значение)
- `section: react` (предлагаемое новое значение)

Для дочерней hook-ветки при этом сохраняется отдельный кластер:

- `section: react-hooks` (предлагаемое новое значение)

До фиксации этих значений в `Controlled Vocabulary` ветку не стоит считать готовой к переносу в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
React (overview)
├── JSX (article)
├── Components and Props (article)
├── React Rendering Model (article)
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

- `React` является естественной канонической обзорной точкой входа для всей ветки.
- `React Hooks` здесь оправдан как вложенный `overview`, потому что внутри hooks уже есть собственный устойчивый набор дочерних статей.
- `JSX`, `Components and Props` и `React Rendering Model` на стартовом этапе лучше держать как обычные `article`, а не выделять для них отдельные подобзоры.
- Структура остается в допустимой минимальной форме: `root overview -> sub-overview -> articles`.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `React Core Concepts` как промежуточный слой только ради симметрии;
- `React State Management` как обзорную ветку, если пока нет самостоятельного корпуса;
- `Class Components`, `Lifecycle Methods`, `Synthetic Events`, `React Reconciliation`, если ветка еще не разрослась до этих тем;
- отдельный `overview` для `Functional Components`, если тема пока естественно встраивается в статьи про rendering model и hooks.

Эти темы можно добавить позже, если ветка реально вырастет.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, их физическое размещение должно следовать алфавитному правилу, а не логической близости в ветке:

```text
02. Corpus Mundi/
├── C/
│   ├── Components and Props.md
│   └── Custom Hooks.md
├── J/
│   └── JSX.md
├── R/
│   ├── React.md
│   ├── React Hooks.md
│   ├── React Rendering Model.md
│   └── Rules of Hooks.md
└── U/
    ├── useState.md
    ├── useEffect.md
    ├── useReducer.md
    ├── useContext.md
    └── useRef.md
```

Логическая ветка при этом всё равно собирается через `parent`.

Локальные вложения при необходимости:

```text
02. Corpus Mundi/R/_resources/React/
```

## Созданные черновые заметки

- `React.md`
- `JSX.md`
- `Components and Props.md`
- `React Rendering Model.md`
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
2. Подтвердить `section: react`.
3. Подтвердить `section: react-hooks`.
4. Решить, какие следующие темы React действительно заслуживают отдельных статей.
5. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
