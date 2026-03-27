---
aliases: []
note_type: overview
area: computer-science
domain: networking
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Computer Science]]"
  - "[[Internet]]"
  - "[[OSI Model]]"
  - "[[Network Topology]]"
  - "[[Network Performance]]"
  - "[[Network Protocols]]"
tags: []
---

# Networking

## Краткое определение области

`Networking` — это domain-root overview для заметок о сетевом взаимодействии: моделях сетевых стеков, устройстве Internet, адресации, маршрутизации и прикладных протоколах.

## Что входит в эту тему

- `[[Internet]]`
- `[[OSI Model]]`
- `[[Network Topology]]`
- `[[Network Performance]]`
- `[[Network Protocols]]`

## Как устроена ветка

- `Networking` удерживает domain-level рамку и не должен сам превращаться в свалку частных протокольных заметок.
- `Internet` собирает operational branch про реальную сеть сетей и Internet protocol suite.
- `OSI Model` остается соседней концептуальной model-веткой для описания сетевых функций по слоям.
- `Network Topology` собирает structural branch про формы организации сетей, различие между physical и logical topology и канонические topology patterns.
- `Network Performance` собирает branch про bandwidth, throughput, latency, jitter и packet loss как базовые метрики сетевого поведения.
- `Network Protocols` собирает branch про семейства сетевых протоколов и их роли в стеке, а не про случайный список отдельных protocol names.

## Рекомендуемый маршрут чтения

1. Начать с `[[Network Topology]]`, если нужен язык для описания формы и связности сети.
2. Затем перейти к `[[Network Performance]]`, если нужен язык для описания capacity и качества доставки.
3. Затем перейти к `[[Network Protocols]]`, если нужен общий язык для описания protocol families.
4. После этого читать `[[Internet]]`, если нужен operational взгляд на современную сеть.
5. Затем перейти к `[[TCP IP Model]]` и связанным статьям внутри Internet-ветки.
6. Затем сопоставить это с `[[OSI Model]]` как с соседней концептуальной моделью.

## Что стоит раскрыть дальше

- [ ] Уточнить границы между `Internet` и `OSI Model`
- [ ] Проверить, когда рядом нужен отдельный узел про `Network Architecture`
- [ ] Проверить, когда рядом нужен отдельный узел про `Network Congestion`
- [ ] Проверить, когда `Network Protocols` пора дробить дальше на concrete protocol notes
- [ ] Проверить `related`
