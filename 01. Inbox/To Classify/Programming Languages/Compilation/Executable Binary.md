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
tags: []
---

# Executable Binary

## Краткое определение

`Executable Binary` — это файл или итоговый двоичный артефакт, подготовленный так, чтобы операционная система или среда выполнения могли загрузить и запустить программу.

## Основная идея или механизм

Executable binary не равен просто machine code: он обычно включает формат файла, метаданные, таблицы символов, секции и результаты linking, необходимые для практического запуска программы.

## Границы темы

- Входит: исполнимый артефакт как результат сборки, связь с linking и загрузкой.
- Не входит: весь runtime execution после старта процесса и детальная модель работы loader.

## Связи с другими заметками

Родительская тема:

`[[Compilation]]`

Связанные заметки:

- `[[Machine Code]]`
- `[[Linking]]`
- `[[Program Translation Pipeline]]`

## Примеры, случаи или следствия

Даже если код уже сгенерирован в инструкции целевой архитектуры, программа может еще не быть готова к запуску, пока не собран итоговый executable binary с корректной структурой и связями.

## Что стоит раскрыть дальше

- [ ] Уточнить связь с object files, static linking и dynamic linking
- [ ] Проверить отличие executable binary от library artifact
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
