---
aliases:
  - Прототипная система JavaScript
note_type: overview
area: computer-science
domain: programming-languages
section: javascript
parent:
status: seed
related:
  - "[[Internal Prototype Slot]]"
  - "[[Proto Accessor]]"
  - "[[Prototype Property]]"
  - "[[Prototype Chain]]"
tags:
  - javascript
  - objects
---

# JavaScript Prototype System

## Краткое определение области

Обзорная заметка для того, как в JavaScript устроены прототипы, наследование через цепочку прототипов и разные механизмы доступа к этой модели.

## Что входит в эту тему

- `[[Internal Prototype Slot]]`
- `[[Proto Accessor]]`
- `[[Prototype Property]]`
- `[[Prototype Chain]]`

## Как устроена ветка

- `Internal Prototype Slot` описывает внутреннюю связь объекта с его прототипом.
- `Proto Accessor` описывает пользовательский доступ к этой связи через legacy-accessor.
- `Prototype Property` описывает отдельное свойство функций-конструкторов.
- `Prototype Chain` объясняет, как из этих элементов складывается модель наследования и поиска свойств.

## Рекомендуемый маршрут чтения

1. Начать с `[[Internal Prototype Slot]]`.
2. Затем сравнить его с `[[Proto Accessor]]` и `[[Prototype Property]]`.
3. После этого перейти к `[[Prototype Chain]]`, чтобы собрать общую картину.

## Соседние overview-ветки

- Пока не добавлены.

## Что стоит раскрыть дальше

- [ ] Проверить границы темы
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
