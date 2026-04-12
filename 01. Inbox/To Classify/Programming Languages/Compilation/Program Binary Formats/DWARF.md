---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Binary Formats]]"
status: seed
related:
  - "[[Program Binary Formats]]"
  - "[[ELF]]"
  - "[[Executable Binary]]"
  - "[[Linking]]"
tags: []
---

# DWARF

## Краткое определение

`DWARF` - это стандартизованный формат представления отладочной информации о скомпилированной программе, ее типах, символах, исходных строках и соответствиях между source code и машинным кодом.

## Основная идея или механизм

DWARF позволяет debugger-ам и другим analysis tools восстанавливать структуру исходной программы по бинарному артефакту без необходимости хранить эту структуру в исполняемом коде в явном, runtime-ориентированном виде.

## Границы темы

- Входит: debug information entries, source mapping и типовая роль DWARF в toolchain.
- Не входит: общий процесс интерактивного debugging как инженерная практика.
- Не входит: сам контейнер бинарного файла; это лучше раскрывать в `[[ELF]]` и общей статье `[[Executable Binary]]`.

## Связи с другими заметками

Родительская тема:

`[[Program Binary Formats]]`

Связанные заметки:

- `[[ELF]]`
- `[[Executable Binary]]`
- `[[Linking]]`

## Примеры, случаи или следствия

- При сборке программы debug information часто сохраняется в секциях ELF, чтобы debugger мог связать machine-level state с исходным кодом.
- Удаление или отделение DWARF-данных обычно уменьшает размер бинарника, но ухудшает качество отладки и postmortem-анализа.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между DWARF и symbol tables
- [ ] Добавить различие между debug information и runtime metadata
- [ ] Проверить, когда рядом нужен отдельный материал про debuggers
- [ ] Проверить `aliases`
