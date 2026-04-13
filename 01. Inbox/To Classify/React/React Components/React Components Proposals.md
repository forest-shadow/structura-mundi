---
aliases:
  - React Component Model
  - Components in React
note_type: overview
area: computer-science
domain: frontend-engineering
section: react
parent: "[[React]]"
status: seed
related:
  - "[[React]]"
  - "[[React Props]]"
  - "[[Functional Components]]"
  - "[[Component Composition]]"
  - "[[Class Components]]"
  - "[[React Higher-Order Component]]"
  - "[[React Rendering Model]]"
tags: []
---

# React Components

## Краткое определение области

`React Components` — это overview-заметка для компонентной модели React, в которой интерфейс описывается через компоненты, их входные данные, формы определения и способы композиции.

## Что входит в эту тему

- `[[React Props]]`
- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Class Components]]`
- `[[React Higher-Order Component]]`

## Логическая структура ветки

Ниже зафиксирована именно логическая структура ветки, а не ее текущее физическое размещение по папкам. Часть узлов уже канонизирована и переведена в `02. Corpus Mundi` со статусом `draft`, а часть остается рабочими заметками в `01. Inbox`.

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

- `React`, `React Components`, `React Rendering Model` и `React Hooks` уже существуют как canonical overview-узлы в `Corpus Mundi` и имеют статус `draft`.
- В компонентной подветке уже канонизированы `React Props` и `React Higher-Order Component`, а `Functional Components`, `Component Composition` и `Class Components` пока остаются в `Inbox` со статусом `draft`.
- В rendering-подветке overview уже переехал в `Corpus Mundi`, но базовые article-узлы `React Render`, `React Reconciliation`, `React State Updates` и `React Component Re-renders` пока остаются в `Inbox` со статусом `seed`.
- В hooks-подветке `React Hooks`, `useState`, `useCallback`, `useMemo` и `useReducer` уже находятся в `Corpus Mundi` как `draft`, а `Rules of Hooks`, `useEffect`, `useContext`, `useRef` и `Custom Hooks` пока еще остаются в `Inbox`.

## Как устроена ветка

- `React Components` лучше держать как обзорный узел, а не как одну большую статью про все аспекты компонентов сразу.
- `React Props` вынесены отдельно, потому что props образуют самостоятельный контракт между компонентами и уже достаточно оформлены, чтобы жить как отдельный canonical article.
- `Functional Components` стоит рассматривать как основную современную форму определения компонентов в React.
- `Class Components` полезно держать рядом как исторически важную, но в основном legacy-форму компонентной модели.
- `Component Composition` описывает общий принцип сборки интерфейса из компонентов и их связей.
- `React Higher-Order Component` остается отдельной статьей про специфический паттерн обёртывания и расширения компонентного поведения.
- Физическое расхождение между `Corpus Mundi` и `Inbox` не ломает эту ветку: онтология собирается через `parent`, `related` и canonical note names, а не через соседство файлов в одной папке.

## Границы темы

- В тему входит компонентная модель React как способ организации UI из переиспользуемых единиц.
- На границе находятся `JSX`, `React Rendering Model` и `React Hooks`: они тесно связаны с компонентами, но описывают другие аспекты React.
- `React Higher-Order Component` не стоит растворять в `Component Composition`, потому что это отдельный reuse-pattern со своей логикой.

## Связи с другими заметками

Родительская тема:

`[[React]]`

Связанные заметки:

- `[[React Props]]`
- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Class Components]]`
- `[[React Higher-Order Component]]`
- `[[React Rendering Model]]`

## Рекомендуемый маршрут чтения

1. Начать с `[[React Components]]` как общей рамки компонентной модели.
2. Затем перейти к `[[React Props]]` и `[[Functional Components]]`.
3. После этого читать `[[Component Composition]]` как тему про сборку UI из компонентов.
4. `[[React Higher-Order Component]]` рассматривать как специальный паттерн переиспользования компонентной логики.
5. `[[Class Components]]` читать как legacy-ветку и исторический контекст.

## Что стоит раскрыть дальше

- [ ] Решить, когда `Functional Components`, `Component Composition` и `Class Components` готовы к переносу в `Corpus Mundi`
- [ ] Решить, когда рядом с `React Higher-Order Component` нужны `Render Props` и `Compound Components`
- [ ] Уточнить связь между компонентной моделью и `React Rendering Model`
- [ ] Нормализовать названия ссылок в оставшихся inbox-заметках вокруг `React Props` и `React Higher-Order Component`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
