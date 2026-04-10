---
aliases:
  - Black-box and White-box Monitoring
  - White-box Monitoring
  - Black-box Monitoring
  - White box and black box monitoring
note_type: article
area: computer-science
domain: distributed-systems
section: service-reliability
parent: "[[Monitoring]]"
status: seed
related:
  - "[[Monitoring]]"
  - "[[Synthetic Monitoring]]"
  - "[[Telemetry]]"
  - "[[Observability]]"
tags:
  - observability
  - reliability
---

# White-box and Black-box Monitoring

## Краткое определение

Каноническая статья для различия между white-box и black-box monitoring как двумя базовыми режимами наблюдения за распределенной системой: через внутренние сигналы и через внешнее поведение.

## Основная идея или механизм

Нужно объяснить, почему это различие важно: white-box monitoring дает подробность о состоянии внутренних компонентов, а black-box monitoring показывает, что реально наблюдает внешний потребитель сервиса.

## Границы темы

- Что относится к внутреннему мониторингу по метрикам, логам и runtime-сигналам.
- Где тема переходит в synthetic monitoring, alerting и observability tooling.

## Связи с другими заметками

Родительская тема:

`[[Monitoring]]`

Связанные заметки:

- `[[Synthetic Monitoring]]`
- `[[Telemetry]]`
- `[[Observability]]`

## Примеры, случаи или следствия

Добавить пример ситуации, где white-box сигналы выглядят нормальными, а black-box проверка уже показывает деградацию пользовательского сценария.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
