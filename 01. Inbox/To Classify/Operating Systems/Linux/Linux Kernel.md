---
aliases:
  - Ядро Linux
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux]]"
status: seed
related:
  - "[[Linux Distribution]]"
  - "[[System Calls]]"
  - "[[Processes and Threads]]"
  - "[[Containerization]]"
tags: []
---
![[01. Inbox/To Classify/Operating Systems/Linux/_resources/67696892dd6bb85860f97556a13cf1e2_MD5.jpg|Linux Architecture Overview]]
# Linux Kernel

## Краткое определение

`Linux Kernel` - это ядро операционной системы Linux, то есть тот программный слой, который управляет процессами, памятью, устройствами, файловыми системами и системными вызовами, связывая user space с аппаратным обеспечением.

## Основная идея или механизм

Ядро Linux не является всей операционной системой в практическом пользовательском смысле. Оно выступает центральным системным механизмом, вокруг которого строятся дистрибутивы, user space и прикладная экосистема. Поэтому отдельная заметка нужна, чтобы не смешивать Linux как ядро с Linux как семейством поставляемых систем.

## Границы темы

- В тему входит Linux как ядро и системный execution layer.
- Рядом находится `[[Linux Distribution]]`, где описывается более широкий способ упаковки и поставки Linux-систем.
- Рядом находятся общие темы `[[System Calls]]`, `[[Processes and Threads]]` и `[[File Systems]]`, которые описывают механизмы не только Linux, но ОС вообще.

## Связи с другими заметками

Родительская тема:

`[[Linux]]`

Связанные заметки:

- `[[Linux Distribution]]`
- `[[System Calls]]`
- `[[Processes and Threads]]`
- `[[Containerization]]`

## Примеры, случаи или следствия

- Контейнеризация в Linux строится не на виртуализации отдельного ядра, а на механизмах самого ядра Linux.
- Системный вызов выступает интерфейсом между приложением и ядром.
- Многие особенности поведения процессов, scheduler и изоляции в Linux определяются именно устройством ядра, а не дистрибутива как упаковки.

## Что стоит раскрыть дальше

- [ ] Добавить границу между kernel space и user space
- [ ] Уточнить связь с `Linux Namespaces` и `cgroups`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
