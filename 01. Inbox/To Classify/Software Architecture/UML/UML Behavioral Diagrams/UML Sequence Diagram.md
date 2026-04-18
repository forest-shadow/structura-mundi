---
aliases:
  - Sequence Diagram
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[UML Behavioral Diagrams]]"
status: seed
related:
  - "[[UML]]"
  - "[[UML Use Case Diagram]]"
  - "[[UML Activity Diagram]]"
tags: []
---

# UML Sequence Diagram

## Краткое определение

`UML Sequence Diagram` - это диаграмма взаимодействий, которая показывает участников сценария и порядок сообщений между ними во времени.

## Основная идея или механизм

Она полезна, когда важно не просто перечислить участников, а зафиксировать последовательность вызовов, точку ветвления, синхронность и возвраты между частями системы.

## Границы темы

- Входит: lifelines, сообщения, активации и временной порядок взаимодействий.
- Не входит: подробное описание всех состояний объекта на протяжении его жизненного цикла; для этого лучше подходит `UML State Machine Diagram`.

## Связи с другими заметками

Родительская тема:

`[[UML Behavioral Diagrams]]`

Связанные заметки:

- `[[UML]]`
- `[[UML Use Case Diagram]]`
- `[[UML Activity Diagram]]`

## Примеры, случаи или следствия

Sequence-диаграмма особенно полезна для описания request flow, взаимодействия между сервисами, orchestration и мест, где появляются latency, retries или дополнительные внешние вызовы.

## Что стоит раскрыть дальше

- [ ] Добавить пример для HTTP-запроса через несколько компонентов
- [ ] Уточнить различие между sequence diagram и activity diagram
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
