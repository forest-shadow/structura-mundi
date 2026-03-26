---
aliases:
  - fetchpriority
  - Priority Hints
note_type: article
area: computer-science
domain: web-platform
section: fetch-priority
parent: "[[Browser Loading Optimization Mechanisms]]"
status: seed
related:
  - "[[Preload]]"
  - "[[Resource Hints]]"
  - "[[Script Loading and Execution Attributes]]"
tags:
  - web
  - performance
---

# Fetch Priority

## Краткое определение

Каноническая статья про механизм `fetchpriority`, которым разработчик подсказывает браузеру относительный приоритет загрузки уже обнаруженного ресурса.

## Основная идея или механизм

`Fetch Priority` не столько помогает браузеру раньше найти ресурс, сколько помогает уточнить, как распределять внимание между уже найденными загрузками. Поэтому он соседствует с `Resource Hints`, но не входит в них.

## Границы темы

- Входит: атрибут `fetchpriority` и его роль в настройке относительного приоритета.
- Не входит: полный разбор всех resource hints.

## Связи с другими заметками

Родительская тема:

`[[Browser Loading Optimization Mechanisms]]`

Связанные заметки:

- `[[Preload]]`
- `[[Resource Hints]]`
- `[[Script Loading and Execution Attributes]]`

## Примеры, случаи или следствия

Полезен, когда ресурс уже открывается браузером естественным образом, но нужно явно подсказать, что он важнее или менее важен относительно соседних загрузок.

## Что стоит раскрыть дальше

- [ ] Добавить сравнение `preload` и `fetchpriority`
- [ ] Проверить, нужна ли позже отдельная заметка про JS `priority`
- [ ] Проверить `aliases`
