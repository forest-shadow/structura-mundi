---
aliases:
  - Cross-Origin Resource Sharing
note_type: overview
area: computer-science
domain: web-platform
section: cors
parent: "[[Web Origin Model]]"
status: seed
related:
  - "[[Same-Origin Policy]]"
  - "[[Preflight Request]]"
  - "[[CORS Request Headers]]"
  - "[[CORS Response Headers]]"
  - "[[Credentialed CORS Requests]]"
tags:
  - web
  - security
---

# CORS

## Краткое определение области

Обзорная заметка для механизма `CORS`, через который браузер разрешает контролируемые cross-origin взаимодействия поверх same-origin policy.

## Что входит в эту тему

- `[[Preflight Request]]`
- `[[CORS Request Headers]]`
- `[[CORS Response Headers]]`
- `[[Credentialed CORS Requests]]`

## Как устроена ветка

- `CORS` служит обзорной рамкой для набора browser/server правил, которые вместе определяют, допустим ли cross-origin доступ.
- Preflight и заголовки лучше держать отдельными `article`, а не смешивать в одну общую статью.
- Более мелкие темы вроде отдельных access-control headers пока не выносятся в собственные заметки.

## Рекомендуемый маршрут чтения

1. Начать с `[[Same-Origin Policy]]`.
2. Затем перейти к общей идее `CORS`.
3. После этого читать `[[Preflight Request]]`.
4. Затем разбирать `[[CORS Request Headers]]`, `[[CORS Response Headers]]` и `[[Credentialed CORS Requests]]`.

## Соседние overview-ветки

- Пока не добавлены, но позже рядом может появиться более общая ветка про browser security.

## Что стоит раскрыть дальше

- [ ] Уточнить границы между CORS и same-origin policy
- [ ] Проверить, не нужна ли отдельная статья про fetch credentials mode
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
