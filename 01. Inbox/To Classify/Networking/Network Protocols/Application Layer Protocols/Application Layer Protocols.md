---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-protocols
parent: "[[Network Protocols]]"
status: seed
related:
  - "[[Network Protocols]]"
  - "[[TCP IP Application Layer]]"
  - "[[Application Layer]]"
  - "[[DNS]]"
  - "[[HTTP]]"
tags: []
---

# Application Layer Protocols

## Краткое определение области

`Application Layer Protocols` — это обзорная заметка о протоколах верхнего уровня, через которые приложения используют сетевое взаимодействие и формируют прикладные сетевые сервисы.

## Что входит в эту тему

- Общая роль application-layer protocols.
- Связь прикладных протоколов с transport layer.
- Сопоставление с `[[TCP IP Application Layer]]` и `[[Application Layer]]`.
- `[[HTTP]]` как отдельная прикладная protocol-ветка.

## Как устроена ветка

- `Application Layer Protocols` удерживает общую рамку для прикладных протоколов как семейства верхнего слоя.
- `HTTP` уже оправдан как отдельная `sub-overview`-ветка, потому что тема быстро распадается на messages, methods, status codes, headers и versions.
- Остальные прикладные протоколы вроде `DNS`, `SMTP` и `DHCP` пока лучше не дробить без плотного корпуса рядом.

## Рекомендуемый маршрут чтения

1. Начать с общей идеи `Application Layer Protocols`.
2. Затем перейти к `[[HTTP]]` как к первой развернутой прикладной protocol-ветке.
3. После этого сопоставить HTTP с `[[TCP IP Application Layer]]` и `[[Application Layer]]`.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом нужны `DNS`, `SMTP` и `DHCP` как отдельные подветки
- [ ] Проверить `related`
