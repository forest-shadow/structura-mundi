---
aliases: []
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Networking]]"
status: seed
related:
  - "[[Reverse Proxy]]"
  - "[[CDN and Edge Cache]]"
  - "[[HTTP Proxy]]"
tags: []
---

# Origin Shielding

## Краткое определение

`Origin Shielding` — это архитектурный прием, при котором перед origin-системой размещается дополнительный промежуточный слой, уменьшающий прямую нагрузку и изоляцию origin от внешнего трафика.

## Основная идея или механизм

Вместо того чтобы разрешать множеству внешних узлов обращаться напрямую к origin, система вводит промежуточный shield-layer. Он может концентрировать cache hits, сглаживать traffic bursts, ограничивать fan-out и уменьшать operational pressure на origin infrastructure.

## Границы темы

- Входит: защита origin через промежуточные traffic layers.
- Не входит: любой reverse proxy по определению; `Reverse Proxy` — лишь одна из возможных связанных тем.

## Связи с другими заметками

Родительская тема:

`[[Networking]]`

Связанные заметки:

- `[[Reverse Proxy]]`
- `[[CDN and Edge Cache]]`
- `[[HTTP Proxy]]`

## Примеры, случаи или следствия

- CDN или reverse proxy layer может использоваться как shielding-tier перед origin.
- Origin shielding снижает прямую нагрузку на origin и улучшает control over traffic concentration.

## Что стоит раскрыть дальше

- [ ] Проверить границу между `Origin Shielding` и `CDN and Edge Cache`
- [ ] Проверить `related`
