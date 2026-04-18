---
aliases:
  - State Machine Diagram
  - State Diagram
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[UML Behavioral Diagrams]]"
status: seed
related:
  - "[[UML]]"
  - "[[UML Activity Diagram]]"
  - "[[UML Sequence Diagram]]"
tags: []
---

# UML State Machine Diagram

## Краткое определение

`UML State Machine Diagram` - это диаграмма, которая показывает допустимые состояния сущности и события, переводящие ее из одного состояния в другое.

## Основная идея или механизм

Она помогает явно зафиксировать жизненный цикл объекта, заказа, сессии или процесса, чтобы не держать неявные переходы только в коде или в голове.

## Границы темы

- Входит: состояния, события, переходы, guards и terminal states.
- Не входит: общий поток большого процесса или последовательность взаимодействий между несколькими участниками; для этого лучше подходят `UML Activity Diagram` и `UML Sequence Diagram`.

## Связи с другими заметками

Родительская тема:

`[[UML Behavioral Diagrams]]`

Связанные заметки:

- `[[UML]]`
- `[[UML Activity Diagram]]`
- `[[UML Sequence Diagram]]`

## Примеры, случаи или следствия

State machine-диаграмма особенно полезна для сущностей с ограниченным набором допустимых переходов: заказ, подписка, пользовательская сессия, background job или workflow instance.

## Что стоит раскрыть дальше

- [ ] Добавить пример жизненного цикла заказа или задачи
- [ ] Уточнить, когда state machine полезнее activity diagram
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
