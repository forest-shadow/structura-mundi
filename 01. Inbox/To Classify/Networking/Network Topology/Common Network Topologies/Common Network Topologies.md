---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: network-topology
parent: "[[Network Topology]]"
status: seed
related:
  - "[[Network Topology]]"
  - "[[Physical and Logical Network Topology]]"
  - "[[Star Network Topology]]"
  - "[[Mesh Network Topology]]"
tags: []
---

# Common Network Topologies

## Краткое определение области

`Common Network Topologies` — это обзорная заметка о канонических схемах организации сетей, которые используются как базовые topology patterns в учебных и инженерных описаниях.

Эти topology patterns не привязаны жестко только к physical topology или только к logical topology: в зависимости от контекста одна и та же именованная схема может использоваться как для описания физической организации сети, так и для описания логической схемы взаимодействия. Само различие между physical topology и logical topology вынесено в `[[Physical and Logical Network Topology]]`.

## Что входит в эту тему

- `[[Point-to-Point Network Topology]]`
- `[[Bus Network Topology]]`
- `[[Star Network Topology]]`
- `[[Ring Network Topology]]`
- `[[Mesh Network Topology]]`
- `[[Tree Network Topology]]`
- `[[Hybrid Network Topology]]`

## Как устроена ветка

- Ветка собирает именованные topology patterns как общие модели сетевой организации, а не как отдельные каталоги физических и логических топологий.
- `Point-to-Point Network Topology` фиксирует предельно простую схему прямой связи между двумя узлами.
- `Bus Network Topology`, `Star Network Topology` и `Ring Network Topology` покрывают классические базовые patterns.
- `Mesh Network Topology` и `Tree Network Topology` вводят более сложные схемы связности и масштабирования.
- `Hybrid Network Topology` нужен как рамка для реальных сетей, которые редко укладываются в один чистый pattern.

## Рекомендуемый маршрут чтения

1. Начать с `[[Point-to-Point Network Topology]]` и `[[Bus Network Topology]]` как самых простых схем.
2. Затем перейти к `[[Star Network Topology]]` и `[[Ring Network Topology]]`.
3. После этого читать `[[Mesh Network Topology]]`, `[[Tree Network Topology]]` и `[[Hybrid Network Topology]]`.

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный узел про `Wireless Mesh Network`
- [ ] Решить, когда рядом нужен `Datacenter Network Topology`
- [ ] Проверить `related`
