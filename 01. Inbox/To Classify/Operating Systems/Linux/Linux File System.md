---
aliases:
  - Linux Filesystem
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux]]"
status: seed
related:
  - "[[Linux]]"
  - "[[File Systems]]"
  - "[[Linux Kernel]]"
  - "[[Linux Distribution]]"
  - "[[System Calls]]"
tags: []
---

# Linux File System

## Краткое определение

`Linux File System` — это статья о том, как общая файловая модель ОС проявляется в среде Linux через иерархию каталогов, mount points, virtual file systems и Linux-specific системные соглашения.

## Основная идея или механизм

В Linux файловая система важна не только как абстракция долговременного хранения, но и как единое namespace-пространство, через которое система организует файлы, устройства, псевдофайловые интерфейсы и точки монтирования.

## Границы темы

- В тему входят directory hierarchy, mount points, роль `/proc`, `/sys`, `/dev`, `/etc`, `/var`, `/home` и общий Linux-specific filesystem view.
- Рядом находится `[[File Systems]]`, но она описывает общую OS-абстракцию, а не Linux-specific устройство файлового пространства.

## Связи с другими заметками

Родительская тема:

`[[Linux]]`

Связанные заметки:

- `[[File Systems]]`
- `[[Linux Kernel]]`
- `[[Linux Distribution]]`
- `[[System Calls]]`

## Примеры, случаи или следствия

Linux показывает, что файловая система в ОС может быть не только местом хранения обычных файлов, но и унифицированным интерфейсом к устройствам, процессной информации и системной конфигурации.

## Что стоит раскрыть дальше

- [ ] Развести physical file system implementation и Linux filesystem hierarchy
- [ ] Проверить, когда отдельно нужны `procfs`, `sysfs` и `Filesystem Hierarchy Standard`
- [ ] Проверить `related`
- [ ] Проверить `aliases`