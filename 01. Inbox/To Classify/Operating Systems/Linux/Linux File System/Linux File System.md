---
aliases:
  - Linux Filesystem
  - Linux Filesystems
note_type: overview
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux]]"
status: seed
related:
  - "[[Linux]]"
  - "[[File Systems]]"
  - "[[Filesystem Hierarchy Standard]]"
  - "[[Linking Files]]"
tags: []
---

# Linux File System

## Краткое определение области

`Linux File System` - это Linux-specific overview про то, как в среде Linux устроено файловое пространство: directory hierarchy, mount points, namespaced paths, file metadata, links и соглашения, через которые файловая абстракция ОС становится практически используемой.

## Что входит в эту тему

- `[[Filesystem Hierarchy Standard]]`
- `[[Linking Files]]`

## Как устроена ветка

- `Linux File System` нужен как локальный `overview`, потому что здесь уже собирается не одна isolated article, а несколько разных, но связанных тем про filesystem layout, ссылки между именами файлов и Linux-specific способы организации namespace.
- `Filesystem Hierarchy Standard` лучше держать обычной `article`, потому что это конкретный стандарт соглашений о назначении каталогов, а не вся Linux filesystem model.
- `Linking Files` оправдан как вложенный `overview`, потому что тема естественно распадается как минимум на `Hard Link` и `Symbolic Link`, а в самой родительской заметке неудобно смешивать общую рамку file links с частными различиями между типами ссылок.
- Общая теория файловых систем остаётся в `[[File Systems]]`, а Linux-specific детали вроде link semantics, mount layout и path conventions лучше удерживать именно внутри этой ветки.

## Рекомендуемый маршрут чтения

1. Начать с `[[File Systems]]`, если нужна общая OS-level рамка.
2. Затем перейти к `[[Linux File System]]`, чтобы увидеть Linux-specific слой поверх общей файловой абстракции.
3. После этого читать `[[Filesystem Hierarchy Standard]]`, если нужен layout каталогов.
4. Затем перейти к `[[Linking Files]]`, а после него к `[[Hard Link]]` и `[[Symbolic Link]]`, если нужен механизм множественных имён и ссылок на пути в Linux.

## Соседние overview-ветки

- `[[Linux]]`
- `[[File Systems]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `procfs`, `sysfs` и `tmpfs`
- [ ] Уточнить границу между `Linux File System` и общей заметкой `File Systems`
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
