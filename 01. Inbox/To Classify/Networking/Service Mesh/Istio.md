---
aliases:
  - Istio Service Mesh
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Service Mesh]]"
status: seed
related:
  - "[[Service Mesh Control Plane]]"
  - "[[Service Mesh Data Plane]]"
  - "[[Proxy]]"
  - "[[TLS Termination]]"
tags: []
---

# Istio

## Краткое определение

`Istio` — это конкретная service mesh-платформа, которая добавляет к взаимодействию сервисов централизованное управление сетевыми политиками, безопасностью, маршрутизацией трафика и наблюдаемостью.

## Основная идея или механизм

Нужно раскрыть, как Istio реализует service mesh через разделение control plane и data plane, какие operational capabilities он добавляет поверх обычного service-to-service networking и почему его нельзя сводить к одному только proxy.

## Границы темы

- Что относится к Istio как к конкретному продукту и экосистеме конфигурации.
- Чем Istio отличается от общего понятия `Service Mesh` и от generic proxying.

## Связи с другими заметками

Родительская тема:

`[[Service Mesh]]`

Связанные заметки:

- `[[Service Mesh Control Plane]]`
- `[[Service Mesh Data Plane]]`
- `[[Proxy]]`
- `[[TLS Termination]]`

## Примеры, случаи или следствия

Добавить 1-3 примера traffic management, mTLS rollout и policy enforcement в сервисной среде.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
