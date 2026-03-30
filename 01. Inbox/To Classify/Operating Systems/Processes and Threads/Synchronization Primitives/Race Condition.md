---
aliases:
  - Race Conditions
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Synchronization Primitives]]"
status: seed
related:
  - "[[Synchronization Primitives]]"
  - "[[Data Race]]"
  - "[[Thread]]"
  - "[[Interprocess Communication]]"
tags: []
---

# Race Condition

## Краткое определение

`Race Condition` — это ошибка корректности, при которой поведение системы зависит от неконтролируемого относительного порядка выполнения нескольких concurrent actors.

## Основная идея или механизм

- несколько потоков, процессов или обработчиков событий работают с общим состоянием или общим протоколом;
- если корректность зависит от конкретного порядка шагов, а система этот порядок не гарантирует, результат становится недетерминированным;
- synchronization primitives нужны именно затем, чтобы ввести ordering, mutual exclusion и наблюдаемую дисциплину доступа.

## Границы темы

- Входит: order-dependent bugs, lost updates, check-then-act ошибки и другие сбои, где interleaving меняет результат.
- Не входит: полный формальный разбор language-specific memory models и lock-free proofs.
- Не всякая `Race Condition` является `Data Race`: ошибка может возникать и на уровне протокола, даже если отдельные операции сами по себе атомарны.

## Связи с другими заметками

Родительская тема:

`[[Synchronization Primitives]]`

Связанные заметки:

- `[[Data Race]]`
- `[[Thread]]`
- `[[Interprocess Communication]]`

## Примеры, случаи или следствия

- Два потока одновременно проверяют, что очередь не пуста, и оба пытаются забрать один и тот же элемент.
- Один поток меняет состояние объекта, а другой читает его в промежуточный момент и принимает неверное решение.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между protocol-level race и `Data Race`
- [ ] Добавить примеры с lock-based и lock-free кодом
- [ ] Проверить `related`
- [ ] Проверить `aliases`
