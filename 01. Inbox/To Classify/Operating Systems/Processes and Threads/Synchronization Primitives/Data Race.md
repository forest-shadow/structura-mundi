---
aliases:
  - Data Races
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[Synchronization Primitives]]"
status: seed
related:
  - "[[Synchronization Primitives]]"
  - "[[Race Condition]]"
  - "[[Thread]]"
  - "[[CPU Scheduling]]"
tags: []
---

# Data Race

## Краткое определение

`Data Race` — это несинхронизированный concurrent access к одной и той же области памяти, где как минимум одно обращение является записью и между операциями не установлено корректное ordering.

## Основная идея или механизм

- два или более потока разделяют одну memory location или одну структуру данных;
- если чтения и записи происходят без mutex, atomic protocol или другого механизма ordering, наблюдаемое значение начинает зависеть от interleaving и низкоуровневого поведения системы;
- поэтому `Data Race` обычно рассматривается как более узкий memory-level случай по отношению к `Race Condition`.

## Границы темы

- Входит: shared-memory read/write и write/write конфликты без должной синхронизации.
- Не входит: любой protocol-level race, где конфликт возникает без прямого состязания за одну memory location.
- Не всякая `Race Condition` является `Data Race`, и не всякий language-level formalism про data races нужно раскрывать в этой заметке.

## Связи с другими заметками

Родительская тема:

`[[Synchronization Primitives]]`

Связанные заметки:

- `[[Race Condition]]`
- `[[Thread]]`
- `[[CPU Scheduling]]`

## Примеры, случаи или следствия

- Два потока инкрементируют общий счётчик без mutex или atomic increment.
- Один поток пишет данные и выставляет флаг готовности, а другой читает флаг и данные без гарантированного ordering.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между `Data Race` и happens-before reasoning
- [ ] Добавить различие между mutex-based и atomic-based защитой
- [ ] Проверить `related`
- [ ] Проверить `aliases`
