---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Machine Code]]"
  - "[[Linking]]"
  - "[[Program Translation Pipeline]]"
  - "[[Program Binary Formats]]"
  - "[[ELF]]"
  - "[[Object File]]"
  - "[[Shared Library]]"
tags: []
---

# Executable Binary

## Краткое определение

`Executable Binary` — это файл или итоговый двоичный артефакт, подготовленный так, чтобы операционная система или среда выполнения могли загрузить и запустить программу.

## Основная идея или механизм

Executable binary не равен просто machine code: он обычно включает формат файла, метаданные, таблицы символов, секции и результаты linking, необходимые для практического запуска программы. При этом он является только одним из видов бинарных артефактов рядом с `[[Object File]]` и `[[Shared Library]]`.

## Границы темы

- Входит: исполнимый артефакт как результат сборки, связь с linking и загрузкой.
- Входит: различие между исполнимым бинарником и другими бинарными артефактами вроде `[[Object File]]` и `[[Shared Library]]`.
- Не входит: весь runtime execution после старта процесса и детальная модель работы loader.
- Не входит: конкретные стандарты контейнера вроде `[[ELF]]`; их лучше раскрывать в `[[Program Binary Formats]]`.

## Связи с другими заметками

Родительская тема:

`[[Compilation]]`

Связанные заметки:

- `[[Machine Code]]`
- `[[Linking]]`
- `[[Program Translation Pipeline]]`
- `[[Program Binary Formats]]`
- `[[ELF]]`
- `[[Object File]]`
- `[[Shared Library]]`

## Примеры, случаи или следствия

Даже если код уже сгенерирован в инструкции целевой архитектуры, программа может еще не быть готова к запуску, пока не собран итоговый executable binary с корректной структурой и связями.

Важное следствие: не всякий бинарный файл, содержащий machine code, является executable binary. Объектный файл или shared library тоже содержат код и метаданные, но выполняют другую роль в toolchain.

## Что стоит раскрыть дальше

- [ ] Уточнить связь с static linking и dynamic linking
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
