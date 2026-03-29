---
aliases:
  - Rendering Tree
note_type: article
area: computer-science
domain: web-platform
section: browser-rendering-pipeline
parent: "[[Browser Rendering Pipeline]]"
status: seed
related:
  - "[[DOM]]"
  - "[[CSSOM]]"
  - "[[Layout]]"
tags:
  - web
  - performance
---

# Render Tree

## Краткое определение

Каноническая статья про `Render Tree` как производную структуру, которую браузер формирует на основе `DOM` и `CSSOM` перед вычислением геометрии и отрисовкой страницы.

## Основная идея или механизм

Эта заметка должна объяснять, почему render tree не совпадает с `DOM` один к одному и как он подготавливает данные для последующих стадий `layout` и `paint`.

## Границы темы

- Входит: связь `DOM`, `CSSOM` и отображаемой структуры.
- Не входит: полный разбор всех причин layout invalidation и paint invalidation.

## Связи с другими заметками

Родительская тема:

`[[Browser Rendering Pipeline]]`

Связанные заметки:

- `[[DOM]]`
- `[[CSSOM]]`
- `[[Layout]]`

## Примеры, случаи или следствия

Добавить примеры, где узлы из `DOM` исключаются из render tree или получают иное влияние на визуальный результат.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
