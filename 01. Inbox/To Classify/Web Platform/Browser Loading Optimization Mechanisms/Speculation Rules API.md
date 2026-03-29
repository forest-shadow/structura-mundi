---
aliases:
  - Speculation Rules
  - speculationrules
note_type: article
area: computer-science
domain: web-platform
section: browser-loading-optimization
parent: "[[Browser Loading Optimization Mechanisms]]"
status: seed
related:
  - "[[Resource Hints]]"
  - "[[Prefetch]]"
  - "[[Lazy Loading]]"
tags:
  - web
  - performance
---

# Speculation Rules API

## Краткое определение

Каноническая статья про `Speculation Rules API`, которым разработчик декларативно описывает, какие будущие навигации браузер может заранее `prefetch` или `prerender`.

## Основная идея или механизм

`Speculation Rules API` ориентирован не на отдельный ресурс, а на вероятный следующий документ. Правила можно задавать через `<script type="speculationrules">` или через HTTP-заголовок `Speculation-Rules`, чтобы браузер заранее подготовил будущий переход.

## Границы темы

- Входит: document-level `prefetch` и `prerender`, правила выбора ссылок и место этого API в оптимизации навигации.
- Не входит: общий разбор client-side routing, data prefetching и всех стратегий ускорения SPA без настоящей навигации документа.

## Связи с другими заметками

Родительская тема:

`[[Browser Loading Optimization Mechanisms]]`

Связанные заметки:

- `[[Resource Hints]]`
- `[[Prefetch]]`
- `[[Lazy Loading]]`

## Примеры, случаи или следствия

Обычно полезен там, где есть несколько высоковероятных следующих переходов, например карточки товаров, оглавление документации или мастер-поток с предсказуемым следующим шагом. В таких сценариях браузер может заранее получить или даже полностью подготовить следующий документ.

## Что стоит раскрыть дальше

- [ ] Добавить сравнение с `link rel="prefetch"` и историческим `prerender`
- [ ] Уточнить поддержку `Speculation-Rules`, CSP и feature detection
- [ ] Проверить `aliases`
