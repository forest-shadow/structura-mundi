---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: internet
parent: "[[Networking]]"
status: seed
related:
  - "[[Networking]]"
  - "[[TCP IP Model]]"
  - "[[OSI Model]]"
  - "[[IP Addressing]]"
  - "[[DNS]]"
  - "[[Routing]]"
tags: []
---

# Internet

## Краткое определение области

`Internet` — это обзорная заметка про глобальную сеть взаимосвязанных сетей, построенную вокруг Internet protocol suite, адресации, маршрутизации и распределенного именования.

## Что входит в эту тему

- `[[TCP IP Model]]`
- `[[IP Addressing]]`
- `[[DNS]]`
- `[[Routing]]`

## Как устроена ветка

- `TCP IP Model` описывает слоистую архитектуру протокольного стека, на котором основана современная Internet.
- `IP Addressing` раскрывает, как узлы и сети получают адресуемость.
- `DNS` объясняет, как символьные имена связываются с сетевой адресацией.
- `Routing` показывает, как пакеты находят путь через множество связанных сетей.

## Рекомендуемый маршрут чтения

1. Начать с `[[TCP IP Model]]`, чтобы зафиксировать стек Internet protocol suite.
2. Затем перейти к `[[IP Addressing]]`.
3. После этого читать `[[Routing]]`.
4. Завершить `[[DNS]]` как слой distributed naming поверх сетевой адресации.

## Соседние overview-ветки

- `[[OSI Model]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про packet switching
- [ ] Решить, когда нужны более узкие notes про `TCP`, `UDP` и `HTTP`
- [ ] Проверить `related`
