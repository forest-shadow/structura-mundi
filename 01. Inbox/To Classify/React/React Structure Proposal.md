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
├── React Components (overview)
│   ├── Props in React (article)
│   ├── Functional Components (article)
│   ├── Component Composition (article)
│   └── Class Components (article)
├── React Rendering Model (overview)
│   ├── React Render (article)
│   ├── React Reconciliation (article)
│   ├── React State Updates (article)
│   ├── React Component Re-renders (article)
│   ├── React Key Prop (article)
│   └── React.memo (article)
└── React Hooks (overview)
    ├── Rules of Hooks (article)
    ├── useState (article)
    ├── useEffect (article)
    ├── useCallback (article)
    ├── useMemo (article)
    ├── useReducer (article)
    ├── useContext (article)
    ├── useRef (article)
    └── Custom Hooks (article)
```

## Почему структура именно такая

- `React` является естественной канонической обзорной точкой входа для всей ветки.
- `React Hooks` оправдан как вложенный `overview`, потому что внутри hooks уже есть собственный устойчивый набор дочерних статей.
- `useMemo` теперь тоже включён в устойчивый hook-кластер, потому что это самостоятельный API с отдельной границей темы.
- `useCallback` теперь тоже включён в устойчивый hook-кластер, потому что это самостоятельный API с отдельной границей темы: стабильность callback references, а не мемоизация значений.
- `React Components` тоже оправдан как вложенный `overview`, потому что прежний узел `Components and Props` смешивал несколько разных объектов знания и лучше работает как связующая рамка.
- `Props in React` вынесены отдельно, поскольку это самостоятельное понятие, а не просто подпункт общего введения.
- `Functional Components` и `Class Components` имеют смысл как отдельные статьи, потому что представляют разные формы компонентной модели.
- `React Rendering Model` теперь оправдан как вложенный `overview`, потому что внутри него уже есть устойчивый набор самостоятельных тем: render, reconciliation, state updates, повторные рендеры и `React.memo`.
- `React Key Prop` оправдан как отдельная соседняя статья внутри `React Rendering Model`: он тесно связан с reconciliation, но ради одной такой темы не стоит превращать `React Reconciliation` в отдельный `overview`.
- `React.memo` остаётся отдельной статьёй внутри этой ветки, потому что это самостоятельный API-узел с собственной границей темы: он относится к повторным рендерам компонентов, а не к hook-кластеру.
- `JSX` остаётся обычной `article`, потому что пока для него не нужен отдельный overview-слой.
- Структура остается в допустимой минимальной форме: `root overview -> sub-overview -> articles`.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `React Core Concepts` как промежуточный слой только ради симметрии;
- `React State Management` как обзорную ветку, если пока нет самостоятельного корпуса;
- `Lifecycle Methods`, `Synthetic Events`, `Render Phase`, если ветка еще не разрослась до этих тем;
- дополнительный `overview` между `React` и `React Components` только ради симметрии;
- отдельные статьи на слишком мелкие формы component API без устойчивого корпуса вокруг них.

Эти темы можно добавить позже, если ветка реально вырастет.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, их физическое размещение должно следовать алфавитному правилу, а не логической близости в ветке:

```text
02. Corpus Mundi/
├── C/
│   ├── Class Components.md
│   ├── Component Composition.md
│   └── Custom Hooks.md
├── F/
│   ├── Functional Components.md
│   └── Props in React.md
├── J/
│   └── JSX.md
├── R/
│   ├── React.md
│   ├── React Components.md
│   ├── React Hooks.md
│   ├── React Component Re-renders.md
│   ├── React Key Prop.md
│   ├── React Reconciliation.md
│   ├── React Render.md
│   ├── React Rendering Model.md
│   ├── React State Updates.md
│   └── React.memo.md
│   └── Rules of Hooks.md
└── U/
    ├── useState.md
    ├── useEffect.md
    ├── useCallback.md
    ├── useMemo.md
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
- `React Components.md`
- `Props in React.md`
- `Functional Components.md`
- `Component Composition.md`
- `Class Components.md`
- `React Rendering Model.md`
- `React Render.md`
- `React Reconciliation.md`
- `React State Updates.md`
- `React Component Re-renders.md`
- `React Key Prop.md`
- `React.memo.md`
- `React Hooks.md`
- `Rules of Hooks.md`
- `useState.md`
- `useEffect.md`
- `useCallback.md`
- `useMemo.md`
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
