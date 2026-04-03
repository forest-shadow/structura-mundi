---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Networking]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Layer 7 Proxy]]"
  - "[[TLS Termination]]"
  - "[[Origin Shielding]]"
tags: []
---

# Service Mesh

## Краткое определение области

`Service Mesh` — это обзорная заметка о сетевом инфраструктурном слое для управления service-to-service communication внутри распределенной системы: маршрутизацией, политиками безопасности, наблюдаемостью и промежуточной обработкой трафика между сервисами.

## Что входит в эту тему

- `[[Service Mesh Control Plane]]`
- `[[Service Mesh Data Plane]]`
- `[[Istio]]`

## Как устроена ветка

- `Service Mesh` оправдан как отдельный overview-узел, потому что здесь естественно собираются темы про control plane, data plane, traffic policy, mTLS и operational observability.
- Эта ветка соседствует с `[[Proxy]]`, но не сводится к нему: mesh включает не только посредники в datapath, но и централизованное управление их конфигурацией.
- `Istio` пока достаточно держать как product-specific `article`, а не разворачивать в отдельное поддерево до появления плотного корпуса по его внутренним ресурсам и механизмам.

## Рекомендуемый маршрут чтения

1. Начать с `[[Service Mesh Control Plane]]`, чтобы зафиксировать слой управления.
2. Затем перейти к `[[Service Mesh Data Plane]]`, чтобы понять, где именно обрабатывается трафик.
3. После этого читать `[[Istio]]` как конкретную реализацию service mesh.

## Соседние overview-ветки

- Родительская рамка: `[[Networking]]`
- Соседняя intermediary-ветка: `[[Proxy]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про mTLS, traffic policy и sidecar-модель
- [ ] Проверить границу между `Service Mesh` и `Proxy`
- [ ] Проверить `related`
