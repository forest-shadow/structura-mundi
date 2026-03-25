---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: performance-optimization
parent: "[[Cache Policies]]"
status: seed
related:
  - "[[Cache Policies]]"
  - "[[Eviction Policies]]"
  - "[[Application Cache]]"
tags: []
---

# Admission Policies

## Краткое определение

`Admission Policies` — это статья о правилах, по которым система решает, какие объекты вообще стоит помещать в кэш.

## Границы темы

- Входит: admission control, filtering low-value entries, protection from cache pollution.
- Не входит: выбор объекта для удаления после того, как он уже был принят в кэш.

## Связи с другими заметками

Родительская тема:

`[[Cache Policies]]`

Связанные заметки:

- `[[Eviction Policies]]`
- `[[Application Cache]]`
- `[[Database Cache]]`

## Примеры, случаи или следствия

- Admission policy особенно важна при bursty workloads и одноразовых ключах.
- Без admission control кэш может быстро заполниться данными без повторного спроса.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужен отдельный article про `TinyLFU Admission`
- [ ] Проверить `related`
