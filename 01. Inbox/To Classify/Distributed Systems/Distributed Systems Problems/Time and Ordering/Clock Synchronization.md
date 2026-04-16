---
aliases:
  - Time Synchronization
  - Clock Sync
note_type: article
area: computer-science
domain: distributed-systems
section: distributed-systems-problems
parent: "[[Time and Ordering]]"
status: seed
related:
  - "[[Time and Ordering]]"
  - "[[UTC]]"
  - "[[Coordination and Consensus]]"
  - "[[Consistency Under Replication]]"
tags:
  - consistency
---

# Clock Synchronization

## Краткое определение

`Clock Synchronization` - это согласование локальных часов разных узлов с общей внешней шкалой времени, обычно выражаемой через `UTC`. В distributed systems эта тема важна потому, что локальные часы дрейфуют, а сетевые задержки делают точное совпадение недостижимым.

## Основная идея или механизм

Система пытается удерживать ошибку локальных часов в приемлемых границах, чтобы timestamps, timeouts, leases и expiration logic работали достаточно надежно. Это не делает время "идеально истинным", а лишь уменьшает рассогласование между узлами и внешней reference-scale.

## Границы темы

- В тему входят drift, skew, приближение локальных часов к внешнему времени и operational trade-offs синхронизации.
- Рядом, но не совпадают с ней, purely logical clocks и причинный порядок событий.

## Связи с другими заметками

Родительская тема:

- `[[Time and Ordering]]`

Связанные заметки:

- `[[UTC]]`
- `[[Coordination and Consensus]]`
- `[[Consistency Under Replication]]`

## Примеры, случаи или следствия

- Lease-based leader election становится ненадежной, если узлы сильно расходятся по локальному времени.
- TTL, token expiration и scheduled retries дают неожиданные эффекты при заметном clock skew.
- Даже хорошая синхронизация часов не заменяет logical ordering там, где важна причинность, а не только близость wall-clock timestamps.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужна отдельная заметка про `NTP`
- [ ] Добавить различие между skew и drift
- [ ] Добавить operational примеры допустимой и недопустимой ошибки часов
- [ ] Проверить `related`
