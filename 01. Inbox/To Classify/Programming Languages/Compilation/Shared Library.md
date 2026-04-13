---
aliases:
  - Shared Object
  - Dynamic Library
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Compilation]]"
  - "[[Linking]]"
  - "[[Object File]]"
  - "[[Executable Binary]]"
  - "[[Program Binary Formats]]"
  - "[[ELF]]"
tags: []
---

# Shared Library

## Краткое определение

`Shared Library` — это бинарный артефакт, содержащий код и экспортируемые symbols в форме, пригодной для повторного использования несколькими программами через dynamic linking и runtime loading.

## Основная идея или механизм

Shared library отделяет переиспользуемую бинарную компоненту от конечного executable: код компонуется в самостоятельный loadable artifact, который может подключаться разными процессами или приложениями без статического вшивания в каждый исполнимый файл.

## Границы темы

- Входит: shared object как результат linking и как единица повторного бинарного использования.
- Входит: отличие shared library от `[[Object File]]` и `[[Executable Binary]]`.
- Не входит: общий процесс dynamic loading целиком как механизм ОС.
- Не входит: конкретный контейнерный стандарт; различие между ELF `.so`, Mach-O `.dylib` и Windows DLL лучше раскрывать в заметках про форматы.

## Связи с другими заметками

Родительская тема:

`[[Compilation]]`

Связанные заметки:

- `[[Linking]]`
- `[[Object File]]`
- `[[Executable Binary]]`
- `[[Program Binary Formats]]`
- `[[ELF]]`

## Примеры, случаи или следствия

- Linker может производить не только executable binary, но и shared library, поэтому эти два артефакта не стоит смешивать.
- В Unix-like toolchains shared library часто реализуется в контейнере ELF, но понятие shared library шире одного конкретного формата файла.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между shared library и static library
- [ ] Добавить связь с dynamic linking и runtime loading
- [ ] Проверить `aliases`
