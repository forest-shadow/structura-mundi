---
aliases:
  - CSS Origin and Importance
  - CSS Cascade Layers and Source Order
  - CSS Cascade Origins and Order
note_type: article
area: computer-science
domain: frontend-engineering
section: css
parent: "[[CSS Cascade]]"
status: seed
related:
  - "[[CSS]]"
  - "[[CSS Cascade]]"
  - "[[CSS Specificity]]"
tags: []
---

# CSS Cascade Origins, Importance, Layers, and Order

## Краткое определение

Каноническая статья про остальные механизмы каскада CSS помимо specificity: origins, importance, cascade layers и source order.

## Основная идея или механизм

Эта заметка должна объяснять, что каскад CSS разрешает конфликт не только через specificity. До сравнения селекторов и после него действуют другие оси приоритета: происхождение правила, признак `!important`, положение в cascade layers и source order.

## Границы темы

- Входит: origins, importance, `!important`, cascade layers и source order как части общей модели cascade.
- Не входит: детальный разбор вычисления specificity.

## Связи с другими заметками

Родительская тема:

`[[CSS Cascade]]`

Связанные заметки:

- `[[CSS]]`
- `[[CSS Cascade]]`
- `[[CSS Specificity]]`

## Примеры, случаи или следствия

- Более специфичное правило может проиграть из-за origin или importance.
- Source order имеет значение только тогда, когда предыдущие механизмы уже не развели конфликт.
- Cascade layers вводят дополнительную ось приоритета, которую нельзя свести к specificity.

## Что стоит раскрыть дальше

- [ ] Уточнить порядок применения origin, importance, layers, specificity и source order
- [ ] Добавить примеры, где specificity проигрывает более ранним механизмам каскада
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
