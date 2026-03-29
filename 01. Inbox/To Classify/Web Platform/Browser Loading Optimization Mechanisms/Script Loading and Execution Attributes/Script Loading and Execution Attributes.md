---
aliases:
  - Script Loading Attributes
note_type: overview
area: computer-science
domain: web-platform
section: script-loading-and-execution
parent: "[[Browser Loading Optimization Mechanisms]]"
status: seed
related:
  - "[[Async Script]]"
  - "[[Defer Script]]"
  - "[[Resource Hints]]"
  - "[[Fetch Priority]]"
tags:
  - web
  - performance
---

# Script Loading and Execution Attributes

## Краткое определение области

Обзорная заметка для атрибутов `<script>`, которые управляют тем, как браузер загружает скрипт параллельно с парсингом документа и в какой момент исполняет его.

## Что входит в эту тему

- `[[Async Script]]`
- `[[Defer Script]]`

## Как устроена ветка

- Эта подветка собирает именно атрибуты поведения `<script>`, а не общие hints про ресурсную загрузку.
- `async` подходит для независимых скриптов, которые можно выполнить сразу после готовности.
- `defer` подходит для скриптов, которым нужен уже распарсенный документ и предсказуемый порядок исполнения.
- `async` и `defer` полезно сравнивать рядом, потому что они похожи по способу загрузки, но различаются по расписанию исполнения.

## Что не входит в эту тему

- `Resource Hints`, потому что это отдельное семейство link-based hints.
- `Fetch Priority`, потому что это отдельный механизм влияния на приоритет загрузки.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Script Loading and Execution Attributes`.
2. Затем читать `[[Async Script]]`.
3. После этого читать `[[Defer Script]]`.

## Соседние overview-ветки

- `[[Resource Hints]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границу между classic scripts и module scripts
- [ ] Проверить, нужен ли позже отдельный узел про inline scripts
- [ ] Проверить `related`
