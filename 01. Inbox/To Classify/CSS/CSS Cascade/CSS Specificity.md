---
aliases:
  - CSS Selector Specificity
  - Selector Specificity
note_type: article
area: computer-science
domain: frontend-engineering
section: css
parent: "[[CSS Cascade]]"
status: seed
related:
  - "[[CSS]]"
  - "[[CSS Cascade]]"
  - "[[CSS Cascade Origins, Importance, Layers, and Order]]"
tags: []
---

# CSS Specificity

## Краткое определение

Каноническая статья про specificity в CSS как механизм сравнения селекторов при конфликте нескольких подходящих правил.

## Основная идея или механизм

Эта заметка должна объяснять, что specificity не определяет весь каскад целиком, а отвечает только за относительный вес конкурирующих селекторов внутри общей модели cascade.

## Границы темы

- Входит: вычисление относительного веса селекторов и роль specificity в выборе правила.
- Не входит: полный разбор source order, `!important`, cascade layers и всех остальных этапов каскада.

## Связи с другими заметками

Родительская тема:

`[[CSS Cascade]]`

Связанные заметки:

- `[[CSS]]`
- `[[CSS Cascade]]`
- `[[CSS Cascade Origins, Importance, Layers, and Order]]`

## Примеры, случаи или следствия

Добавить примеры сравнения селекторов по specificity и случаи, где более специфичное правило всё равно проигрывает из-за других механизмов каскада.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить примеры сравнения селекторов
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
