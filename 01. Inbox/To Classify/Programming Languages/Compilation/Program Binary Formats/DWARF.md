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

- Входит: debug information entries, source mapping, call frame information и типовая роль DWARF в toolchain.
- Входит: разграничение между богатой debug information и более узким разговорным выражением debugging symbols.
- Не входит: общий процесс интерактивного debugging как инженерная практика.
- Не входит: сам контейнер бинарного файла; это лучше раскрывать в `[[ELF]]` и общей статье `[[Executable Binary]]`.
- Не входит: отдельный общий обзор по всем форматам debug information; такой узел имеет смысл заводить только если рядом появятся другие самостоятельные форматы.

## Связи с другими заметками

Родительская тема:

`[[Program Binary Formats]]`

Связанные заметки:

- `[[ELF]]`
- `[[Executable Binary]]`
- `[[Linking]]`

## Примеры, случаи или следствия

- При сборке программы debug information часто сохраняется в секциях ELF, чтобы debugger мог связать machine-level state с исходным кодом.
- В инженерной речи DWARF часто нестрого называют debugging symbols, но это неточно: symbol names составляют только часть той debug information, которую описывает стандарт.
- Удаление или отделение DWARF-данных обычно уменьшает размер бинарника, но ухудшает качество отладки и postmortem-анализа.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между DWARF и symbol tables
- [ ] Проверить, когда рядом нужен отдельный материал про debuggers
- [ ] Проверить `aliases`
