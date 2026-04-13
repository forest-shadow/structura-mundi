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
  - "[[Props in React]]"
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

- `[[Props in React]]`
- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Class Components]]`
- `[[Higher-Order Component]]`

## Как устроена ветка

- `React Components` лучше держать как обзорный узел, а не как одну большую статью про все аспекты компонентов сразу.
- `Props in React` вынесены отдельно, потому что props образуют самостоятельный контракт между компонентами.
- `Functional Components` стоит рассматривать как основную современную форму определения компонентов в React.
- `Class Components` полезно держать рядом как исторически важную, но в основном legacy-форму компонентной модели.
- `Component Composition` описывает общий принцип сборки интерфейса из компонентов и их связей.
- `Higher-Order Component` остается отдельной статьей про специфический паттерн обёртывания и расширения компонентного поведения.

## Границы темы

- В тему входит компонентная модель React как способ организации UI из переиспользуемых единиц.
- На границе находятся `JSX`, `React Rendering Model` и `React Hooks`: они тесно связаны с компонентами, но описывают другие аспекты React.
- `Higher-Order Component` не стоит растворять в `Component Composition`, потому что это отдельный reuse-pattern со своей логикой.

## Связи с другими заметками

Родительская тема:

`[[React]]`

Связанные заметки:

- `[[Props in React]]`
- `[[Functional Components]]`
- `[[Component Composition]]`
- `[[Class Components]]`
- `[[Higher-Order Component]]`
- `[[React Rendering Model]]`

## Рекомендуемый маршрут чтения

1. Начать с `[[React Components]]` как общей рамки компонентной модели.
2. Затем перейти к `[[Props in React]]` и `[[Functional Components]]`.
3. После этого читать `[[Component Composition]]` как тему про сборку UI из компонентов.
4. `[[Higher-Order Component]]` рассматривать как специальный паттерн переиспользования компонентной логики.
5. `[[Class Components]]` читать как legacy-ветку и исторический контекст.

## Что стоит раскрыть дальше

- [ ] Проверить, нужна ли отдельная статья `Props in React`, если файл еще не создан
- [ ] Решить, когда рядом с `Higher-Order Component` нужны `Render Props` и `Compound Components`
- [ ] Уточнить связь между компонентной моделью и `React Rendering Model`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
