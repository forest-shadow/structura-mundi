---
aliases: []
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[Software Architecture]]"
status: seed
related:
  - "[[Finite Automaton]]"
  - "[[UML State Machine Diagram]]"
  - "[[Event-Driven Architecture]]"
  - "[[Client-Server Model]]"
tags: []
---

# State Machine

## Краткое определение

`State Machine` - это инженерная модель поведения системы, в которой допустимые состояния, события и переходы между ними задаются явно.

## Основная идея или механизм

Такая модель помогает описывать поведение не как хаотический набор условных веток, а как ограниченный граф допустимых переходов. Это особенно полезно там, где система реагирует на события, проходит через жизненный цикл и не должна попадать в невалидные комбинации состояний.

## Границы темы

- Входит: явное моделирование состояний, событий, переходов, guards и правил допустимого поведения объекта или процесса.
- Близко, но не совпадает: `[[Finite Automaton]]` как строгая формальная модель из теории автоматов и `[[UML State Machine Diagram]]` как конкретная визуальная нотация для представления такой модели.

## Связи с другими заметками

Родительская тема:

`[[Software Architecture]]`

Связанные заметки:

- `[[Finite Automaton]]`
- `[[UML State Machine Diagram]]`
- `[[Event-Driven Architecture]]`
- `[[Client-Server Model]]`

## Примеры, случаи или следствия

State machine особенно полезна для описания жизненного цикла заказа, пользовательской сессии, background job, сетевого соединения, workflow instance или UI-компонента с ограниченным набором допустимых переходов.

## Что стоит раскрыть дальше

- [ ] Добавить пример с состояниями, событиями и невалидными переходами
- [ ] Уточнить границу между state machine, workflow и event-driven process
- [ ] Проверить, когда рядом нужны `Hierarchical State Machine` и `Statechart`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
