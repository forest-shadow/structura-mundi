---
aliases:
  - Component Diagram
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[UML Structural Diagrams]]"
status: seed
related:
  - "[[UML]]"
  - "[[UML Deployment Diagram]]"
  - "[[Clean Architecture]]"
tags: []
---

# UML Component Diagram

## Краткое определение

`UML Component Diagram` - это диаграмма, которая показывает крупные программные компоненты системы, их интерфейсы и зависимости между ними.

## Основная идея или механизм

Она помогает подняться выше уровня отдельных классов и зафиксировать архитектурные блоки: сервисы, модули, адаптеры, библиотеки и точки взаимодействия между ними.

## Границы темы

- Входит: компоненты, предоставляемые и требуемые интерфейсы, зависимости между крупными частями системы.
- Не входит: физическое размещение компонентов на узлах развертывания; это отдельный вопрос для `UML Deployment Diagram`.

## Связи с другими заметками

Родительская тема:

`[[UML Structural Diagrams]]`

Связанные заметки:

- `[[UML]]`
- `[[UML Deployment Diagram]]`
- `[[Clean Architecture]]`

## Примеры, случаи или следствия

Компонентная диаграмма полезна для описания границ между application layer, adapters, infrastructure modules и внешними интеграциями.

## Что стоит раскрыть дальше

- [ ] Добавить пример для layered architecture
- [ ] Уточнить отличие component diagram от package diagram и deployment diagram
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
