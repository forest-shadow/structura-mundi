---
aliases:
  - Activity Diagram
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[UML Behavioral Diagrams]]"
status: seed
related:
  - "[[UML]]"
  - "[[UML Sequence Diagram]]"
  - "[[UML State Machine Diagram]]"
tags: []
---

# UML Activity Diagram

## Краткое определение

`UML Activity Diagram` - это диаграмма потока действий, которая показывает шаги процесса, развилки, параллельные ветви и точки синхронизации.

## Основная идея или механизм

Она удобна, когда нужно описать не обмен сообщениями между участниками, а логику самого процесса: какие действия выполняются, в какой очередности и при каких условиях путь меняется.

## Границы темы

- Входит: действия, переходы, развилки, условия, параллельные ветви и join/split-точки.
- Не входит: детальная модель структурных отношений между сущностями и компонентами; это вопрос для structural-диаграмм.

## Связи с другими заметками

Родительская тема:

`[[UML Behavioral Diagrams]]`

Связанные заметки:

- `[[UML]]`
- `[[UML Sequence Diagram]]`
- `[[UML State Machine Diagram]]`

## Примеры, случаи или следствия

Activity-диаграмма полезна для описания бизнес-процесса, pipeline обработки задачи, approval flow или многоветвистого backend workflow.

## Что стоит раскрыть дальше

- [ ] Добавить пример с условиями и параллельными ветвями
- [ ] Уточнить границу между activity diagram и flowchart
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
