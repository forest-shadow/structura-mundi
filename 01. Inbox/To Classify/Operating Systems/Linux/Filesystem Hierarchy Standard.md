---
aliases:
  - FHS
  - Filesystem Hierarchy Standard (FHS)
  - Стандарт иерархии файловой системы
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux File System]]"
status: seed
related:
  - "[[Linux]]"
  - "[[Linux File System]]"
  - "[[Linux Distribution]]"
  - "[[File Systems]]"
tags: []
---

# Filesystem Hierarchy Standard

## Краткое определение

`Filesystem Hierarchy Standard` (FHS) - это стандарт соглашений о назначении ключевых каталогов и расположении файлов в Unix-like/Linux файловой иерархии.

## Основная идея или механизм

FHS описывает не конкретную реализацию файловой системы вроде ext4 или XFS, а логический layout корневого дерева: какие типы данных и системных артефактов должны находиться в `/etc`, `/usr`, `/var`, `/home`, `/opt`, `/srv`, `/tmp` и других каталогах.

## Границы темы

- Входит: назначение ключевых каталогов, различие между configuration/state/static data, связь FHS с Linux-дистрибутивами.
- Не входит: внутренняя реализация VFS, inode model, journaling и on-disk filesystem formats.
- Не входит: вся Linux filesystem model; она раскрывается в `[[Linux File System]]`.

## Связи с другими заметками

Родительская тема:

`[[Linux File System]]`

Связанные заметки:

- `[[Linux]]`
- `[[Linux Distribution]]`
- `[[File Systems]]`

## Примеры, случаи или следствия

Добавить разбор нескольких устойчивых каталогов:

- `/etc` как пространство локальной конфигурации;
- `/var` как пространство изменяемого состояния;
- `/usr` как пространство shareable/static userland-содержимого;
- `/home` как пространство пользовательских данных;
- `/run` как пространство runtime-состояния текущей загрузки.

## Что стоит раскрыть дальше

- [ ] Уточнить статус FHS как стандарта и его связь с практикой конкретных дистрибутивов
- [ ] Добавить таблицу ключевых каталогов
- [ ] Развести FHS, Linux File System и конкретные on-disk filesystems
- [ ] Проверить `aliases`
