---
aliases:
  - DI
note_type: overview
area: computer-science
domain: software-architecture
section: dependency-management
parent: "[[Dependency Management]]"
status: seed
related:
  - "[[Composition Root]]"
  - "[[Dependency Inversion Principle]]"
  - "[[Inversion of Control]]"
  - "[[Service Locator]]"
tags: []
---

# Dependency Injection

## Краткое определение области

Обзорная заметка для практики, при которой объект получает зависимости извне, а не создает их самостоятельно внутри своей бизнес-логики.

## Что входит в эту тему

- `[[Composition Root]]`

## Как устроена ветка

- `Dependency Injection` реализует одну из наиболее полезных практических форм `Inversion of Control`.
- Эта практика помогает применять `Dependency Inversion Principle` в реальном коде.
- `Composition Root` выступает как естественная дочерняя тема, потому что DI отвечает на вопрос "как передавать зависимости", а composition root отвечает на вопрос "где их связывать в приложение".

## Что не входит в эту тему

- `Service Locator`, потому что это соседний и обычно менее предпочтительный способ доступа к зависимостям.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Dependency Injection`.
2. Затем перейти к `[[Composition Root]]`.
3. После этого сравнить с `[[Service Locator]]`.

## Соседние overview-ветки

- `[[Design Principles]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, нужен ли позже отдельный узел для constructor injection
- [ ] Проверить, нужен ли позже отдельный узел для dependency injection containers
- [ ] Проверить `related`
