# React Structure Proposal

## Назначение

Этот файл фиксирует рабочую иерархию заметок для темы `React` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё ещё требуется подтверждённая словарная рамка:

- `area: computer-science`
- `domain: frontend-engineering`
- `section: react`
- `section: react-hooks`

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
│   └── Virtual DOM (article)
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

- `React` выступает корневым `overview` для всей ветки.
- `React Components` нужен как связующий обзорный узел для компонентной модели, а не как одна общая статья про всё сразу.
- `React Rendering Model` лучше держать отдельным `overview`, потому что внутри него уже есть устойчивый набор тем: render, reconciliation, state updates и повторные рендеры.
- `Virtual DOM` корректнее держать как отдельную `article` внутри `React Rendering Model`, а не как синоним всей rendering-модели React.
- `React Hooks` остаётся отдельным `overview`, потому что это самостоятельный API-кластер со своими правилами и устойчивым набором дочерних тем.

## Что не стоит создавать заранее

- промежуточные overview-слои только ради симметрии;
- отдельные статьи на слишком мелкие аспекты reconciliation, пока они не образуют устойчивый корпус;
- дополнительные группировки hooks вроде `Performance Hooks` или `Effect Hooks`, если под ними ещё нет плотной подветки.

## Что создано в рамках этой итерации

- `React.md`
- `React Rendering Model.md`
- `Virtual DOM.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: frontend-engineering`.
2. Подтвердить `section: react`.
3. Подтвердить `section: react-hooks`.
4. Досоздать недостающие stubs для уже принятой React-иерархии.
5. После этого переводить заметки из `seed` в рабочие черновики.
