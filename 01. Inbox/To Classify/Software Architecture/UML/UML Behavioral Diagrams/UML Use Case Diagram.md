---
aliases:
  - Use Case Diagram
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[UML Behavioral Diagrams]]"
status: seed
related:
  - "[[UML]]"
  - "[[UML Sequence Diagram]]"
  - "[[Client-Server Model]]"
tags: []
---

# UML Use Case Diagram

## Краткое определение

`UML Use Case Diagram` - это диаграмма, которая показывает акторов, границу системы и ключевые сценарии взаимодействия с ней.

## Основная идея или механизм

Она нужна не для внутренней реализации, а для фиксации того, какие цели поддерживает система и кто с ней взаимодействует снаружи.

## Границы темы

- Входит: акторы, use cases и внешняя граница системы.
- Не входит: порядок внутренних вызовов и детальная логика обработки сценария; это лучше раскрывать через `UML Sequence Diagram` или `UML Activity Diagram`.

## Связи с другими заметками

Родительская тема:

`[[UML Behavioral Diagrams]]`

Связанные заметки:

- `[[UML]]`
- `[[UML Sequence Diagram]]`
- `[[Client-Server Model]]`

## Примеры, случаи или следствия

Use case-диаграмма полезна, когда нужно отделить внешний контракт системы от внутренней реализации и быстро показать ключевые сценарии для пользователя, администратора или соседнего сервиса.

## Что стоит раскрыть дальше

- [ ] Добавить пример для веб-приложения с несколькими ролями
- [ ] Уточнить границу между use case diagram и user journey
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
