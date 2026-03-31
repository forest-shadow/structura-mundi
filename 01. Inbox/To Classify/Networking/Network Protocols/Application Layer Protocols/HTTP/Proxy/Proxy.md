---
aliases:
  - Proxy Server
note_type: overview
area: computer-science
domain: networking
section: network-protocols
parent: "[[HTTP]]"
status: seed
related:
  - "[[HTTP]]"
  - "[[HTTP Messages]]"
  - "[[Forward Proxy]]"
  - "[[Reverse Proxy]]"
tags: []
---

# Proxy

## Краткое определение области

`Proxy` — это обзорная заметка о промежуточном узле, который принимает HTTP-запросы и передает их дальше от имени одной из сторон взаимодействия. Внутри этой темы важно различать, чью сторону представляет посредник: клиента или origin-сервер.

## Что входит в эту тему

- `[[Forward Proxy]]`
- `[[Reverse Proxy]]`

## Как устроена ветка

- `Proxy` удерживает общую рамку для HTTP-посредников и не сводится только к одному deployment-сценарию.
- `Forward Proxy` описывает прокси со стороны клиента, где посредник управляет исходящим доступом, анонимизацией или политиками выхода во внешнюю сеть.
- `Reverse Proxy` описывает прокси со стороны сервера, где посредник принимает внешний трафик, скрывает origin-инстансы и берет на себя часть инфраструктурных функций.
- Более узкие разновидности вроде transparent proxy, caching proxy или chained proxy пока не выносятся в отдельные notes, чтобы ветка не росла преждевременно.

## Рекомендуемый маршрут чтения

1. Начать с общей рамки `Proxy`.
2. Затем прочитать `[[Forward Proxy]]`, чтобы увидеть клиентскую сторону посредничества.
3. После этого перейти к `[[Reverse Proxy]]`, чтобы сопоставить server-side роль с client-side ролью.
4. Затем вернуться к `[[HTTP]]` и `[[HTTP Messages]]`, если нужно закрепить место proxy-узлов в request-response модели.

## Соседние overview-ветки

- Родительская рамка: `[[HTTP]]`
- Более широкая protocol-рамка: `[[Application Layer Protocols]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `Proxy Authentication`
- [ ] Решить, когда нужен отдельный article про `CONNECT Tunneling`
- [ ] Проверить, нужны ли рядом `Load Balancer` и `API Gateway`
- [ ] Проверить `related`
