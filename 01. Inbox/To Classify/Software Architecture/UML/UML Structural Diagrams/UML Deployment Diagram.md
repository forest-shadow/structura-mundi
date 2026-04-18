---
aliases:
  - Deployment Diagram
note_type: article
area: computer-science
domain: software-architecture
section: architecture-modeling
parent: "[[UML Structural Diagrams]]"
status: seed
related:
  - "[[UML]]"
  - "[[UML Component Diagram]]"
  - "[[Client-Server Model]]"
tags: []
---

# UML Deployment Diagram

## Краткое определение

`UML Deployment Diagram` - это диаграмма, которая показывает, на каких узлах развертывания размещаются программные артефакты и как между собой связаны вычислительные среды.

## Основная идея или механизм

Она переводит архитектурную схему в инфраструктурный вопрос: где исполняется код, какие узлы взаимодействуют и как логические компоненты соотносятся с физическим или виртуальным окружением.

## Границы темы

- Входит: узлы, среды исполнения, развертываемые артефакты и связи между ними.
- Не входит: внутренний контракт компонентов или детализация классов; эти вопросы лучше раскрывать через `UML Component Diagram` и `UML Class Diagram`.

## Связи с другими заметками

Родительская тема:

`[[UML Structural Diagrams]]`

Связанные заметки:

- `[[UML]]`
- `[[UML Component Diagram]]`
- `[[Client-Server Model]]`

## Примеры, случаи или следствия

Deployment-диаграмма особенно полезна, когда нужно развести application server, database server, external gateway, worker nodes и другие точки исполнения по средам и каналам связи.

## Что стоит раскрыть дальше

- [ ] Добавить пример для веб-приложения с отдельной БД и worker-процессом
- [ ] Уточнить разницу между deployment diagram и infrastructure topology sketch
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
