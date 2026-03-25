---
aliases:
  - Domain Name System
note_type: overview
area: computer-science
domain: networking
section: dns
parent: "[[Internet]]"
status: seed
related:
  - "[[Internet]]"
  - "[[IP Addressing]]"
  - "[[Routing]]"
  - "[[DNS Resolution]]"
  - "[[Recursive Resolver]]"
tags: []
---

# DNS

## Краткое определение области

`DNS` — это обзорная заметка о Domain Name System как распределенной системе именования в Internet. Она собирает под одной рамкой процесс разрешения имен, роли резолверов и авторитативных серверов, а также базовые сущности вроде записей и зон.

## Что входит в эту тему

- `[[DNS Resolution]]`
- `[[Recursive Resolver]]`
- `[[Authoritative DNS Server]]`
- `[[DNS Resource Record]]`
- `[[DNS Zone]]`

## Как устроена ветка

- `DNS Resolution` фиксирует основной процесс преобразования имени в данные о целевом узле.
- `Recursive Resolver` и `Authoritative DNS Server` разделяют две главные операционные роли внутри системы.
- `DNS Resource Record` и `DNS Zone` описывают базовые единицы данных и административной организации пространства имен.
- Более узкие operational и security-темы пока не выносятся в отдельные статьи, чтобы ветка не разрасталась преждевременно.

## Рекомендуемый маршрут чтения

1. Начать с `[[DNS Resolution]]`, чтобы увидеть общую механику работы DNS.
2. Затем перейти к `[[Recursive Resolver]]` и `[[Authoritative DNS Server]]`.
3. После этого читать `[[DNS Resource Record]]` и `[[DNS Zone]]`.
4. Затем сопоставить DNS с `[[IP Addressing]]` и `[[Routing]]` как соседними Internet-механизмами.

## Соседние overview-ветки

- Родительская рамка: `[[Internet]]`
- `[[TCP IP Model]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Root Name Server`, `TLD Name Server` и `DNSSEC`
- [ ] Проверить, не нужен ли отдельный article про `TTL`
- [ ] Проверить `related`
