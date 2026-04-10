---
aliases:
  - Synthetic Checks
  - Синтетический мониторинг
note_type: article
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Monitoring]]"
status: seed
related:
  - "[[Monitoring]]"
  - "[[White-box and Black-box Monitoring]]"
  - "[[Dashboard]]"
  - "[[Service Reliability]]"
tags:
  - observability
  - reliability
---

# Synthetic Monitoring

## Краткое определение

Каноническая статья для synthetic monitoring как активного наблюдения за системой через регулярные внешние проверки, эмулирующие пользовательские или контрактные сценарии.

## Основная идея или механизм

Нужно объяснить, почему synthetic monitoring важен именно для распределенных систем: он проверяет не внутреннюю телеметрию компонентов, а наблюдаемое поведение всей цепочки снаружи.

## Границы темы

- Что относится к synthetic probes, canary checks и scripted journeys.
- Где тема переходит в black-box monitoring, alerting и end-to-end testing.

## Связи с другими заметками

Родительская тема:

`[[Monitoring]]`

Связанные заметки:

- `[[White-box and Black-box Monitoring]]`
- `[[Dashboard]]`
- `[[Service Reliability]]`

## Примеры, случаи или следствия

Добавить пример проверки логина, checkout-flow или health endpoint с нескольких региональных точек наблюдения.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
