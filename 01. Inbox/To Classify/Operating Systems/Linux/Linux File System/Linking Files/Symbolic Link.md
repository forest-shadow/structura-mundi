---
aliases:
  - Soft Link
  - Symlink
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linking Files]]"
status: draft
related:
  - "[[Linux File System]]"
  - "[[Linking Files]]"
  - "[[Hard Link]]"
tags: []
---

# Symbolic Link

## Краткое определение

`Symbolic Link` - это специальный файловый объект в Linux, который хранит ссылку на целевой путь и разрешается системой как косвенный переход к другой цели.

## Основная идея или механизм

Symbolic link не делит тот же inode с целевым regular file. Вместо этого он хранит pathname, который должен быть отдельно разрешён. Поэтому symbolic link может указывать на каталог, на файл в другой файловой системе или даже на несуществующую цель.

## Границы темы

- Входит: path-based indirection, broken symlinks и поведение при переименовании или удалении target path.
- Входит: различие между symbolic link и hard link.
- Не входит: общая рамка Linux file links; она находится в `[[Linking Files]]`.

## Связи с другими заметками

Родительская тема:

`[[Linking Files]]`

Связанные заметки:

- `[[Linux File System]]`
- `[[Hard Link]]`

## Примеры, случаи или следствия

- Symbolic link может вести на цель в другой файловой системе, где hard link невозможен.
- Если целевой путь исчезает или переименовывается, symlink может стать broken link.
- Символьные ссылки часто используются для удобных alias-путей, совместимости layout и перенаправления конфигурационных или исполняемых файлов.

## Что стоит раскрыть дальше

- [ ] Уточнить роль pathname resolution
- [ ] Добавить примеры абсолютных и относительных symbolic links
- [ ] Проверить `aliases`
- [ ] Проверить `related`
