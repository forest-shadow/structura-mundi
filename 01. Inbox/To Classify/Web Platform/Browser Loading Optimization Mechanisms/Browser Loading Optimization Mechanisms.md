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
  - "[[Early Hints]]"
  - "[[Fetch Priority]]"
  - "[[Lazy Loading]]"
  - "[[Script Loading and Execution Attributes]]"
  - "[[Speculation Rules API]]"
tags:
  - web
  - performance
---

# Browser Loading Optimization Mechanisms

## Краткое определение области

Обзорная заметка про механизмы, которыми разработчик влияет на обнаружение ресурсов, сетевые приоритеты, расписание исполнения и отложенную или спекулятивную загрузку во время работы браузера со страницей.

## Терминологическая оговорка

Для удобства эту ветку можно нестрого обобщать как `browser hints`, но это не имя одного канонического стандарта. Внутри неё лучше различать link-based hints, HTTP-механизмы ранней передачи подсказок, декларативную спекулятивную навигацию и стратегии отложенной загрузки.

## Что входит в эту тему

- `[[Resource Hints]]`
- `[[Early Hints]]`
- `[[Fetch Priority]]`
- `[[Lazy Loading]]`
- `[[Script Loading and Execution Attributes]]`
- `[[Speculation Rules API]]`

## Как устроена ветка

- `Browser Loading Optimization Mechanisms` служит практической рамкой внутри более общего узла `Browser Page Processing`.
- `Resource Hints` остаётся каноническим названием для семейства link-based hints про раннее обнаружение ресурсов, прогрев соединений и упреждающую загрузку.
- `Early Hints` вынесен отдельно, потому что это HTTP-механизм с предварительным ответом `103`, который может доставить `Link`-подсказки раньше основного ответа.
- `Fetch Priority` остаётся отдельным механизмом настройки приоритета и не сводится к `Resource Hints`.
- `Lazy Loading` собирает стратегии отложенной загрузки некритичных ресурсов и потому не прячется ни внутрь `Resource Hints`, ни внутрь атрибутов `<script>`.
- Атрибуты `async` и `defer` относятся к поведению `<script>` и потому собраны в отдельной подветке `Script Loading and Execution Attributes`.
- `Speculation Rules API` описывает document-level prefetch и prerender для вероятных будущих навигаций и потому тоже живёт рядом, а не внутри `Resource Hints`.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Browser Loading Optimization Mechanisms`.
2. Затем перейти к `[[Resource Hints]]`.
3. После этого читать `[[Early Hints]]`.
4. Затем перейти к `[[Fetch Priority]]`.
5. После этого перейти к `[[Script Loading and Execution Attributes]]`.
6. Затем читать `[[Lazy Loading]]`.
7. После этого перейти к `[[Speculation Rules API]]`.

## Соседние overview-ветки

- `[[Browser Rendering]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границу между `Prefetch` и `Speculation Rules API`
- [ ] Решить, нужен ли позже отдельный узел про исторический `prerender`
- [ ] Проверить `related`
