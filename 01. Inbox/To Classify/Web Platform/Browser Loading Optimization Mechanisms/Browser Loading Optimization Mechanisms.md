---
aliases:
  - Browser Loading Hints
  - Browser Hints
note_type: overview
area: computer-science
domain: web-platform
section: browser-loading-optimization
parent: "[[Browser Page Processing]]"
status: seed
related:
  - "[[Browser Rendering]]"
  - "[[Resource Hints]]"
  - "[[Fetch Priority]]"
  - "[[Script Loading and Execution Attributes]]"
tags:
  - web
  - performance
---

# Browser Loading Optimization Mechanisms

## Краткое определение области

Обзорная заметка про механизмы, которыми разработчик влияет на обнаружение ресурсов, сетевые приоритеты и расписание исполнения во время загрузки страницы.

## Терминологическая оговорка

Для удобства эту ветку можно нестрого обобщать как `browser hints`, но это не имя одного канонического стандарта. Внутри неё лучше различать официальные семейства и отдельные механизмы вроде `[[Resource Hints]]`, `[[Fetch Priority]]` и атрибутов загрузки и исполнения `<script>`.

## Что входит в эту тему

- `[[Resource Hints]]`
- `[[Fetch Priority]]`
- `[[Script Loading and Execution Attributes]]`

## Как устроена ветка

- `Browser Loading Optimization Mechanisms` служит практической рамкой внутри более общего узла `Browser Page Processing`.
- `Resource Hints` остаётся каноническим названием для семейства hints про раннее обнаружение ресурсов, прогрев соединений и упреждающую загрузку.
- `Fetch Priority` остаётся отдельным механизмом настройки приоритета и не сводится к `Resource Hints`.
- Атрибуты `async` и `defer` относятся к поведению `<script>` и поэтому собраны в отдельной подветке `Script Loading and Execution Attributes`, а не внутри `Resource Hints`.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Browser Loading Optimization Mechanisms`.
2. Затем перейти к `[[Resource Hints]]`.
3. После этого читать `[[Fetch Priority]]`.
4. Затем перейти к `[[Script Loading and Execution Attributes]]`.

## Соседние overview-ветки

- `[[Browser Rendering]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный узел про `Early Hints`
- [ ] Проверить, нужна ли позже отдельная заметка про `Speculation Rules API`
- [ ] Уточнить, когда имеет смысл добавить сюда `lazy loading`
- [ ] Проверить `related`
