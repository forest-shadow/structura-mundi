---
aliases:
  - Распределенная транзакция
  - 2PC
  - Two-Phase Commit
note_type: article
area: computer-science
domain: distributed-systems
section: dual-write
parent: "[[Dual Write]]"
status: seed
related:
  - "[[Dual Write]]"
  - "[[Transactional Outbox]]"
tags: []
---

# Distributed Transaction

## Краткое определение

Distributed Transaction - это механизм, который пытается обеспечить согласованное подтверждение изменений сразу в нескольких участниках или ресурсах.

## Основная идея или механизм

Нужно раскрыть, почему distributed transaction выглядит как прямой ответ на проблему dual write и почему во многих распределенных системах предпочитают избегать этого пути.

## Границы темы

- Что относится к distributed transaction.
- Чем этот подход отличается от outbox plus relay patterns.

## Связи с другими заметками

Родительская тема:

`[[Dual Write]]`

Связанные заметки:

- `[[Dual Write]]`
- `[[Transactional Outbox]]`

## Примеры, случаи или следствия

Добавить 1-3 сценария, где согласованность достигается за счет координации нескольких ресурсов.

## Что стоит раскрыть дальше

- [ ] Уточнить определение.
- [ ] Добавить связи.
- [ ] Проверить `aliases`.
- [ ] Проверить `tags`.
