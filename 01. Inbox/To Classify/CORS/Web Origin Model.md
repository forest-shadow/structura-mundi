---
aliases: []
note_type: overview
area: computer-science
domain: web-platform
section: web-origin-model
parent: "[[Frontend Engineering]]"
status: seed
related:
  - "[[Web Origin]]"
  - "[[Same-Origin Policy]]"
  - "[[CORS]]"
tags:
  - web
  - security
---

# Web Origin Model

## Краткое определение области

Обзорная заметка для модели browser-origin, через которую браузер различает same-origin и cross-origin взаимодействия и накладывает соответствующие ограничения.

## Что входит в эту тему

- `[[Web Origin]]`
- `[[Same-Origin Policy]]`
- `[[CORS]]`

## Как устроена ветка

- `Web Origin Model` служит верхнеуровневой рамкой для origin-based ограничений и разрешений.
- Базовые понятия `origin` и `same-origin policy` остаются обычными `article`.
- `CORS` выделен в дочерний `overview`, потому что имеет собственный устойчивый набор механизмов.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Web Origin Model`.
2. Затем перейти к `[[Web Origin]]`.
3. После этого читать `[[Same-Origin Policy]]`.
4. Затем входить в `[[CORS]]` и его дочерние статьи.

## Соседние overview-ветки

- Позже рядом могут появиться более широкие ветки про browser security или web platform networking, но сейчас они не нужны.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между origin model и broader browser security
- [ ] Проверить, нужен ли отдельный узел про cookies and credentials
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
