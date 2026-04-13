---
aliases:
  - Executable and Linkable Format
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Binary Formats]]"
status: seed
related:
  - "[[Program Binary Formats]]"
  - "[[Executable Binary]]"
  - "[[Linking]]"
  - "[[DWARF]]"
  - "[[Object File]]"
  - "[[Shared Library]]"
tags: []
---

# ELF

## Краткое определение

`ELF` - это стандартный бинарный формат, в котором Unix-like системы обычно представляют object files, shared libraries, core dumps и исполнимые файлы.

## Основная идея или механизм

ELF задает структуру бинарного артефакта через заголовки, секции и сегменты, благодаря чему toolchain, linker, loader и debugger могут одинаково интерпретировать содержимое файла.

## Границы темы

- Входит: ELF как формат контейнера для code, symbols, relocation data и debug sections.
- Входит: использование одного и того же формата ELF для разных видов артефактов вроде `[[Object File]]`, `[[Shared Library]]` и `[[Executable Binary]]`.
- Не входит: весь процесс linking или вся модель runtime loading целиком.
- Не входит: сами виды артефактов как отдельные понятия; различие между `[[Object File]]`, `[[Shared Library]]` и `[[Executable Binary]]` лучше раскрывать в их собственных заметках.
- Не входит: сама debug information как отдельный стандарт; это лучше раскрывать в `[[DWARF]]`.

## Связи с другими заметками

Родительская тема:

`[[Program Binary Formats]]`

Связанные заметки:

- `[[Executable Binary]]`
- `[[Linking]]`
- `[[DWARF]]`
- `[[Object File]]`
- `[[Shared Library]]`

## Примеры, случаи или следствия

- Один и тот же формат ELF может использоваться не только для конечного executable, но и для `[[Object File]]` и `[[Shared Library]]`.
- Отладочные секции в ELF часто содержат данные в формате `[[DWARF]]`.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между sections и segments
- [ ] Проверить, когда рядом нужен отдельный материал про symbol tables и relocations
- [ ] Проверить `aliases`
