---
aliases:
  - inode
  - Index Node
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux File System]]"
status: seed
related:
  - "[[Linux File System]]"
  - "[[Linking Files]]"
  - "[[Hard Link]]"
  - "[[Symbolic Link]]"
tags: []
---

# Inode

## Краткое определение

`Inode` - это структура метаданных файлового объекта в Unix-like файловой системе, которая хранит его идентичность и атрибуты отдельно от строкового имени в каталоге.

## Основная идея или механизм

Разделение `inode` и directory entry позволяет Linux различать имя файла и сам файловый объект, благодаря чему hard links могут давать одному и тому же объекту несколько имен, а pathname resolution не сводится к простой строковой подстановке.

## Границы темы

- Входит: inode как носитель file metadata, link count и identity внутри файловой системы.
- Входит: связь inode с hard links и границами одной mounted filesystem.
- Не входит: полный on-disk layout каждой конкретной filesystem implementation.

## Связи с другими заметками

Родительская тема:

`[[Linux File System]]`

Связанные заметки:

- `[[Linking Files]]`
- `[[Hard Link]]`
- `[[Symbolic Link]]`

## Примеры, случаи или следствия

- Несколько hard links могут указывать на один и тот же `inode`, оставаясь равноправными именами одного файлового объекта.
- Символическая ссылка имеет собственный `inode`, но хранит путь к другой цели, а не делит с ней одну идентичность.
- Жесткие ссылки обычно не могут пересекать границы файловых систем, потому что `inode` идентичен только внутри конкретной filesystem.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между inode, directory entry и pathname resolution
- [ ] Проверить, когда рядом нужен отдельный материал про dentry
- [ ] Проверить границу между общей темой `File Systems` и Linux-specific моделью inode
- [ ] Проверить `aliases`
