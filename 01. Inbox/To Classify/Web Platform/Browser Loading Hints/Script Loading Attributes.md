---
aliases: []
note_type: overview
area: computer-science
domain: web-platform
section: script-loading
parent: "[[Browser Loading Hints]]"
status: seed
related:
  - "[[Async Script]]"
  - "[[Defer Script]]"
tags:
  - web
  - performance
---

# Script Loading Attributes

## Краткое определение области

Обзорная заметка для атрибутов загрузки и исполнения `<script>`, которые влияют на порядок выполнения и блокировку парсинга документа.

## Что входит в эту тему

- `[[Async Script]]`
- `[[Defer Script]]`

## Как устроена ветка

- Эта подветка собирает только устойчивые атрибуты поведения скриптов.
- Сравнение `async` и `defer` лучше держать в обзорной рамке, а не выносить в отдельный канонический узел.
- Пока сюда не добавляются более редкие или косвенно связанные механизмы.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Script Loading Attributes`.
2. Затем читать `[[Async Script]]`.
3. После этого читать `[[Defer Script]]`.

## Соседние overview-ветки

- `[[Resource Hints]]`

## Что стоит раскрыть дальше

- [ ] Уточнить различие между download order и execution order
- [ ] Проверить, нужна ли позже заметка про module scripts
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
