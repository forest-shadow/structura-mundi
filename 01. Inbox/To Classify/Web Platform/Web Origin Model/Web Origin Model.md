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
- Базовые понятия `origin`, `same-origin policy` и `CORS` остаются обычными `article`.
- Темы вроде preflight, CORS headers и credentialed requests пока раскрываются как разделы внутри `CORS`, а не как отдельная подветка.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Web Origin Model`.
2. Затем перейти к `[[Web Origin]]`.
3. После этого читать `[[Same-Origin Policy]]`.
4. Затем читать `[[CORS]]` как статью про контролируемый cross-origin доступ.

## Соседние overview-ветки

- Позже рядом могут появиться более широкие ветки про browser security или web platform networking, но сейчас они не нужны.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между origin model и broader browser security
- [ ] Проверить, нужен ли отдельный узел про cookies and credentials
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
