---
aliases:
  - lazy loading
  - loading="lazy"
note_type: article
area: computer-science
domain: web-platform
section: browser-loading-optimization
parent: "[[Browser Loading Optimization Mechanisms]]"
status: seed
related:
  - "[[Preload]]"
  - "[[Fetch Priority]]"
  - "[[Script Loading and Execution Attributes]]"
tags:
  - web
  - performance
---

# Lazy Loading

## Краткое определение

Каноническая статья про `lazy loading` как стратегию отложенной загрузки некритичных ресурсов до момента, когда они действительно понадобятся пользователю или приблизятся к viewport.

## Основная идея или механизм

`Lazy Loading` уменьшает объём работы на старте страницы: браузер или приложение не загружает всё сразу, а откладывает часть изображений, iframe, медиа или кода до более позднего момента. На практике это может выражаться и через нативный `loading="lazy"`, и через более общие стратегии отложенной загрузки.

## Границы темы

- Входит: нативный lazy loading для изображений и iframe, а также общая идея deferred loading для некритичных ресурсов.
- Не входит: полный разбор code splitting, маршрутизации и всех прикладных стратегий progressive hydration.

## Связи с другими заметками

Родительская тема:

`[[Browser Loading Optimization Mechanisms]]`

Связанные заметки:

- `[[Preload]]`
- `[[Fetch Priority]]`
- `[[Script Loading and Execution Attributes]]`

## Примеры, случаи или следствия

Обычно полезен для изображений ниже первого экрана, встроенных iframe, неключевых видео и частей JavaScript, которые можно загрузить позже. При этом важно не лениво загружать действительно критические ресурсы первого экрана.

## Что стоит раскрыть дальше

- [ ] Добавить сравнение `loading="lazy"` и eager-загрузки с `fetchpriority`
- [ ] Уточнить границу между lazy loading медиа и lazy loading JavaScript
- [ ] Проверить `aliases`
