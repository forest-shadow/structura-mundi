---
aliases: []
note_type: overview
area: computer-science
domain: system-design
section: dependency-management
parent: "[[System Design]]"
status: seed
related:
  - "[[Inversion of Control]]"
  - "[[Dependency Injection]]"
  - "[[Service Locator]]"
  - "[[Composition Root]]"
  - "[[Dependency Inversion Principle]]"
tags: []
---

# Dependency Management

## Краткое определение области

Обзорная заметка для практик, через которые приложение организует зависимости между своими компонентами, выбирает реализации и собирает рабочий объектный граф.

## Что входит в эту тему

- `[[Inversion of Control]]`
- `[[Dependency Injection]]`
- `[[Service Locator]]`
- `[[Composition Root]]`

## Как устроена ветка

- `Inversion of Control` задает более общую рамку передачи контроля над зависимостями.
- `Dependency Injection` выступает как основной желательный способ явной передачи зависимостей.
- `Composition Root` уточняет, где именно приложение должно собираться в единый working graph.
- `Service Locator` полезно держать рядом как соседний и обычно менее желательный способ доступа к зависимостям.

## Рекомендуемый маршрут чтения

1. Начать с `[[Inversion of Control]]`.
2. Затем перейти к `[[Dependency Injection]]`.
3. После этого читать `[[Composition Root]]`.
4. Затем сравнить с `[[Service Locator]]`.

## Соседние overview-ветки

- `[[Design Principles]]`

## Что стоит раскрыть дальше

- [ ] Решить, нужен ли позже отдельный узел для dependency injection containers
- [ ] Проверить, нужна ли позже заметка про application bootstrap
- [ ] Проверить `related`
