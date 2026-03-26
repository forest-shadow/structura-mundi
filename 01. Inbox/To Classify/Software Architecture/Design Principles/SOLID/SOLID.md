---
aliases: []
note_type: overview
area: computer-science
domain: software-architecture
section: design-principles
parent: "[[Design Principles]]"
status: seed
related:
  - "[[Single Responsibility Principle]]"
  - "[[Open-Closed Principle]]"
  - "[[Liskov Substitution Principle]]"
  - "[[Interface Segregation Principle]]"
  - "[[Dependency Inversion Principle]]"
tags: []
---

# SOLID

## Краткое определение области

Обзорная заметка для семейства из пяти принципов объектно-ориентированного проектирования, которые помогают управлять ответственностью модулей, степенью связности и направлением зависимостей.

## Что входит в эту тему

- `[[Single Responsibility Principle]]`
- `[[Open-Closed Principle]]`
- `[[Liskov Substitution Principle]]`
- `[[Interface Segregation Principle]]`
- `[[Dependency Inversion Principle]]`

## Как устроена ветка

- `SOLID` полезно держать как компактный sub-overview, потому что пять принципов обычно обсуждаются вместе и образуют устойчивый концептуальный пакет.
- Первые четыре принципа больше связаны с формой модулей, интерфейсов и расширения поведения.
- `Dependency Inversion Principle` особенно важен как мост к ветке `Dependency Management`, `Dependency Injection` и `Composition Root`.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `SOLID`.
2. Затем читать `[[Single Responsibility Principle]]` и `[[Open-Closed Principle]]`.
3. После этого перейти к `[[Liskov Substitution Principle]]` и `[[Interface Segregation Principle]]`.
4. Завершить чтением `[[Dependency Inversion Principle]]` как принципа, который сильнее всего пересекается с архитектурой зависимостей.

## Соседние overview-ветки

- `[[Dependency Management]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, нужна ли позже отдельная заметка про историю SOLID
- [ ] Проверить, не стоит ли позже связать ветку с refactoring smells
- [ ] Проверить `related`
