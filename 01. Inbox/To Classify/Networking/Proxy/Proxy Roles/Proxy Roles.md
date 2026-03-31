---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Forward Proxy]]"
  - "[[Reverse Proxy]]"
tags: []
---

# Proxy Roles

## Краткое определение области

`Proxy Roles` — это обзорная заметка о том, какую сторону взаимодействия представляет прокси и где находится его trust boundary.

## Что входит в эту тему

- `[[Forward Proxy]]`
- `[[Reverse Proxy]]`

## Как устроена ветка

- `Forward Proxy` описывает посредника со стороны клиента.
- `Reverse Proxy` описывает посредника со стороны сервера.
- Такое разделение является базовым, потому что от него зависят модель доступа, политика безопасности и характер функций прокси.

## Рекомендуемый маршрут чтения

1. Начать с различия между client-side и server-side proxying.
2. Затем прочитать `[[Forward Proxy]]`.
3. После этого перейти к `[[Reverse Proxy]]`.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли рядом отдельный article про `Egress Proxy`
- [ ] Проверить, нужен ли рядом отдельный article про `Ingress Proxy`
- [ ] Проверить `related`
