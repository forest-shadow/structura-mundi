# React Structure Proposal

## Назначение

Этот файл фиксирует рабочую иерархию заметок для темы `React` по правилам `Principia Rerum`.

Сейчас ветка находится в смешанном состоянии: часть заметок уже переведена в `02. Corpus Mundi` и получила статус `draft`, а часть остается в `01. Inbox` как рабочие `seed`- или `draft`-черновики. Поэтому ниже зафиксирована прежде всего логическая структура ветки, а не только текущее размещение файлов.

Для этой ветки уже подтверждена словарная рамка:

- `area: computer-science`
- `domain: frontend-engineering`
- `section: react`
- `section: react-hooks`

## Логическая структура ветки

```text
React (overview, Corpus Mundi, draft)
├── JSX (article, Corpus Mundi, draft)
├── React Components (overview, Corpus Mundi, draft)
│   ├── React Props (article, Corpus Mundi, draft)
│   ├── Functional Components (article, Inbox, draft)
│   ├── Component Composition (article, Inbox, draft)
│   ├── Class Components (article, Inbox, draft)
│   └── React Higher-Order Component (article, Corpus Mundi, draft)
├── React Rendering Model (overview, Corpus Mundi, draft)
│   ├── React Render (article, Inbox, seed)
│   ├── React Reconciliation (article, Inbox, seed)
│   ├── React State Updates (article, Inbox, seed)
│   ├── React Component Re-renders (article, Inbox, seed)
│   ├── React Key Prop (article, Corpus Mundi, draft)
│   ├── React.memo (article, Corpus Mundi, draft)
│   └── Virtual DOM (article, Corpus Mundi, draft)
└── React Hooks (overview, Corpus Mundi, draft)
    ├── Rules of Hooks (article, Inbox, seed)
    ├── useState (article, Corpus Mundi, draft)
    ├── useEffect (article, Inbox, seed)
    ├── useCallback (article, Corpus Mundi, draft)
    ├── useMemo (article, Corpus Mundi, draft)
    ├── useReducer (article, Corpus Mundi, draft)
    ├── useContext (article, Inbox, seed)
    ├── useRef (article, Inbox, seed)
    └── Custom Hooks (article, Inbox, seed)
```

## Текущее состояние ветки

- Корневые overview-узлы `React`, `React Components`, `React Rendering Model` и `React Hooks` уже находятся в `Corpus Mundi` и имеют статус `draft`.
- В компонентной ветке уже канонизированы `React Props` и `React Higher-Order Component`, а `Functional Components`, `Component Composition` и `Class Components` пока остаются в `Inbox` как `draft`.
- В rendering-ветке обзор уже канонизирован, но четыре базовых article-заметки про сам процесс обновления пока находятся в `Inbox` как `seed`.
- В hooks-ветке часть базовых API уже переехала в `Corpus Mundi`, тогда как `Rules of Hooks`, `useEffect`, `useContext`, `useRef` и `Custom Hooks` остаются в `Inbox`.

## Почему структура именно такая

- `React` выступает корневым `overview` для всей ветки.
- `React Components` нужен как связующий обзорный узел для компонентной модели, а не как одна общая статья про всё сразу.
- `React Higher-Order Component` корректнее держать внутри `React Components`, потому что его главным объектом является сам компонент как абстракция: HOC принимает компонент и возвращает новый компонент, а значит относится к паттернам организации компонентной модели, а не к hook-ветке.
- `React Rendering Model` лучше держать отдельным `overview`, потому что внутри него уже есть устойчивый набор тем: render, reconciliation, state updates, повторные рендеры, identity-механизмы вроде `React Key Prop` и оптимизационные узлы вроде `React.memo`.
- `Virtual DOM` корректнее держать как отдельную `article` внутри `React Rendering Model`, а не как синоним всей rendering-модели React.
- `React Key Prop` тоже корректно держать внутри `React Rendering Model`, потому что по смыслу он относится к identity элементов в reconciliation, а не к общей теме props.
- `React.memo` тоже корректно держать внутри `React Rendering Model`, потому что по смыслу он относится к модели повторных рендеров компонентов, а не к hook-ветке.
- Хотя `React.memo` формально имеет форму HOC-обёртки, в онтологии ветки его лучше не подчинять статье `Higher-Order Component`: это специальный API React для пропуска повторных рендеров, а не общий паттерн переиспользования компонентной логики.
- `React Hooks` остаётся отдельным `overview`, потому что это самостоятельный API-кластер со своими правилами и устойчивым набором дочерних тем.
- Смешанное физическое состояние ветки допустимо: каноническая структура определяется связями `parent` и принятыми note names, а не тем, лежат ли все файлы уже в одной и той же директории.

## Что не стоит создавать заранее

- промежуточные overview-слои только ради симметрии;
- отдельные статьи на слишком мелкие аспекты reconciliation, пока они не образуют устойчивый корпус;
- дополнительные группировки hooks вроде `Performance Hooks` или `Effect Hooks`, если под ними ещё нет плотной подветки.

## Что уже канонизировано в Corpus Mundi

- `React.md`
- `JSX.md`
- `React Components.md`
- `React Props.md`
- `React Higher-Order Component.md`
- `React Rendering Model.md`
- `React Hooks.md`
- `React Key Prop.md`
- `React.memo.md`
- `Virtual DOM.md`
- `useState.md`
- `useCallback.md`
- `useMemo.md`
- `useReducer.md`

## Что пока остается в Inbox

- `Functional Components.md`
- `Component Composition.md`
- `Class Components.md`
- `React Render.md`
- `React Reconciliation.md`
- `React State Updates.md`
- `React Component Re-renders.md`
- `Rules of Hooks.md`
- `useEffect.md`
- `useContext.md`
- `useRef.md`
- `Custom Hooks.md`

## Следующий шаг

1. Довести оставшиеся `seed`-заметки в `Inbox` до содержательного `draft`.
2. Проверить и нормализовать naming consistency между `React Props`, `React Higher-Order Component` и ссылками из старых inbox-файлов.
3. После этого переносить оставшиеся дочерние статьи в `Corpus Mundi` без изменения их логических родителей.
