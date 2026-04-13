---
aliases:
  - Object Module
  - Relocatable Object File
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Compilation]]"
  - "[[Program Translation Pipeline]]"
  - "[[Linking]]"
  - "[[Machine Code]]"
  - "[[Executable Binary]]"
  - "[[Program Binary Formats]]"
  - "[[ELF]]"
tags: []
---

# Object File

## Краткое определение

`Object File` — это бинарный артефакт, содержащий скомпилированный код, данные, символы и relocation information в форме, пригодной прежде всего для последующего linking, а не для непосредственного запуска как программы.

## Основная идея или механизм

Object file фиксирует результат компиляции или ассемблирования отдельной единицы программы в частично подготовленном виде: machine-level content уже существует, но внешние ссылки, итоговые адреса и финальная компоновка еще не завершены.

## Границы темы

- Входит: relocatable binary artifact, symbols, sections и relocation data как типичный вход для `[[Linking]]`.
- Входит: роль object file как промежуточного результата между `[[Machine Code]]` и более законченными артефактами вроде `[[Executable Binary]]` и `[[Shared Library]]`.
- Не входит: финальная модель загрузки и исполнения программы.
- Не входит: конкретный стандарт контейнера сам по себе; это лучше раскрывать в `[[ELF]]` и соседних заметках про форматы.

## Связи с другими заметками

Родительская тема:

`[[Compilation]]`

Связанные заметки:

- `[[Program Translation Pipeline]]`
- `[[Linking]]`
- `[[Machine Code]]`
- `[[Executable Binary]]`
- `[[Program Binary Formats]]`
- `[[ELF]]`

## Примеры, случаи или следствия

- Типичный C/C++ toolchain сначала производит object files, а уже затем linker собирает из них executable binary или shared library.
- Один и тот же понятийный объект `Object File` может реализовываться разными форматами контейнера, поэтому не стоит смешивать эту заметку с `[[ELF]]`.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между object files и symbol resolution
- [ ] Добавить различие между relocatable object и static library
- [ ] Проверить `aliases`
