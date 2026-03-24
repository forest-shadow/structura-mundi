# React Structure Proposal

## Назначение

Этот файл фиксирует рабочую иерархию заметок для темы `React` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, но её словарная рамка уже подтверждена в `Controlled Vocabulary`:

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
│   ├── Class Components (article)
│   └── Higher-Order Component (article)
├── React Rendering Model (overview)
│   ├── React Render (article)
│   ├── React Reconciliation (article)
│   ├── React State Updates (article)
│   ├── React Component Re-renders (article)
│   ├── React Key Prop (article)
│   ├── React.memo (article)
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
- `Higher-Order Component` корректнее держать внутри `React Components`, потому что его главным объектом является сам компонент как абстракция: HOC принимает компонент и возвращает новый компонент, а значит относится к паттернам организации компонентной модели, а не к hook-ветке.
- `React Rendering Model` лучше держать отдельным `overview`, потому что внутри него уже есть устойчивый набор тем: render, reconciliation, state updates, повторные рендеры, identity-механизмы вроде `React Key Prop` и оптимизационные узлы вроде `React.memo`.
- `Virtual DOM` корректнее держать как отдельную `article` внутри `React Rendering Model`, а не как синоним всей rendering-модели React.
- `React Key Prop` тоже корректно держать внутри `React Rendering Model`, потому что по смыслу он относится к identity элементов в reconciliation, а не к общей теме props.
- `React.memo` тоже корректно держать внутри `React Rendering Model`, потому что по смыслу он относится к модели повторных рендеров компонентов, а не к hook-ветке.
- Хотя `React.memo` формально имеет форму HOC-обёртки, в онтологии ветки его лучше не подчинять статье `Higher-Order Component`: это специальный API React для пропуска повторных рендеров, а не общий паттерн переиспользования компонентной логики.
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

1. Досоздать недостающие stubs для уже принятой React-иерархии.
2. После этого переводить заметки из `seed` в рабочие черновики.

# React Components

 [[React Components]] — Обзорная заметка для компонентной модели React, в которой интерфейс строится из компонентов, а связанные с ними понятия вроде `props`, композиции и разновидностей компонентов образуют отдельную подветку.

## Что входит в эту тему

- `[[Props in React]]`
- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Class Components]]`
- `[[Higher-Order Component]]`

## Как устроена ветка

- `React Components` служит связующим `overview`, а не самостоятельной статьёй про один объект знания.
- `Props in React` вынесены отдельно, потому что это самостоятельное понятие, а не просто часть общего введения.
- `Functional Components` и `Class Components` разделены как разные формы компонентной модели.
- `Component Composition` остаётся отдельной статьёй про способ сборки UI из компонентов.
- `Higher-Order Component` стоит держать рядом как отдельную статью про паттерн обёртывания и расширения компонентов, а не растворять его внутри `Component Composition` или `Functional Components`.

## Рекомендуемый маршрут чтения

1. Начать с общего места `React Components`.
2. Затем перейти к `[[Props in React]]` и `[[Functional Components]]`.
3. После этого читать `[[Component Composition]]` и `[[Higher-Order Component]]`.
4. `[[Class Components]]` рассматривать как legacy-ветку, а не как центральную модель современного React.

# React Rendering Model

[[React Rendering Model]] — Обзорная заметка про то, как React вычисляет новое представление интерфейса, сопоставляет его с предыдущим и приводит UI к новому состоянию.

## Что входит в эту тему

- `[[React Render]]`
- `[[React Reconciliation]]`
- `[[React State Updates]]`
- `[[React Component Re-renders]]`
- `[[React Key Prop]]`
- `[[React.memo]]`
- `[[Virtual DOM]]`

## Как устроена ветка

- `React Rendering Model` служит обзорной рамкой для тем про render, reconciliation, state updates, повторные рендеры, identity-механизмы вроде `React Key Prop` и локальные оптимизации вроде `React.memo`.
- `Virtual DOM` полезно держать рядом как объясняющую статью про промежуточное представление UI, но не как замену всей rendering-модели.
- `React Key Prop` стоит держать рядом как отдельную статью про identity элементов в процессе reconciliation, а не как подпункт общей статьи про props.
- `React.memo` тоже стоит держать рядом как отдельную статью про оптимизацию повторных рендеров на границе компонента, а не смешивать его с hooks или общей темой props.
- Более узкие темы внутри reconciliation стоит выносить только тогда, когда они образуют самостоятельный корпус, а не просто удобный подпункт объяснения.

## Рекомендуемый маршрут чтения

1. Начать с `React Rendering Model`.
2. Затем читать `[[React Render]]` и `[[React Reconciliation]]`.
3. После этого перейти к `[[React State Updates]]`, `[[React Component Re-renders]]`, `[[React Key Prop]]` и `[[React.memo]]`.
4. `[[Virtual DOM]]` использовать как поясняющую статью про внутреннее представление и историческую рамку объяснения.
