---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linking Files]]"
status: draft
related:
  - "[[Linux File System]]"
  - "[[Linking Files]]"
  - "[[Symbolic Link]]"
tags: []
---

# Hard Link

## Краткое определение

`Hard Link` - это дополнительное имя того же файлового объекта в файловой системе Linux, при котором несколько directory entries указывают на один и тот же inode.

## Основная идея или механизм

Hard link не создаёт новый независимый файл по содержимому. Он создаёт ещё одну ссылку на тот же самый filesystem object, поэтому удаление одного имени не уничтожает данные, пока остаются другие hard links.

## Границы темы

- Входит: связь hard link с inode, link count и поведением при удалении имени файла.
- Входит: ограничения на создание hard links для каталогов и across-filesystem cases.
- Не входит: symbolic path indirection; это раскрывается в `[[Symbolic Link]]`.

## Связи с другими заметками

Родительская тема:

`[[Linking Files]]`

Связанные заметки:

- `[[Linux File System]]`
- `[[Symbolic Link]]`

## Примеры, случаи или следствия

- Один и тот же файл может иметь несколько имён в одном filesystem, и все они ведут к одному inode.
- Удаление одного пути уменьшает link count, но сами данные исчезают только когда не остаётся ни ссылок, ни открытых дескрипторов.
- Hard links обычно нельзя создавать между разными файловыми системами.

## Что стоит раскрыть дальше

- [ ] Уточнить связь с inode и directory entry
- [ ] Добавить Linux-specific ограничения на hard links to directories
- [ ] Проверить `related`
- [ ] Проверить `aliases`
