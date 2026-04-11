---
aliases:
  - File Linking
  - File Links
note_type: overview
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux File System]]"
status: seed
related:
  - "[[Linux File System]]"
  - "[[Hard Link]]"
  - "[[Symbolic Link]]"
  - "[[File Systems]]"
tags: []
---

# Linking Files

## Краткое определение области

`Linking Files` - это локальный overview про механизмы, которыми Linux позволяет связать имя файла с уже существующим файловым объектом или путём, не копируя содержимое как отдельный новый файл.

## Что входит в эту тему

- `[[Hard Link]]`
- `[[Symbolic Link]]`

## Как устроена ветка

- `Linking Files` нужен как промежуточный `overview`, потому что тема file links в Linux естественно распадается на два разных механизма с разной семантикой разрешения имени и поведения при удалении исходного пути.
- `Hard Link` описывает ещё одно directory entry для того же файлового объекта.
- `Symbolic Link` описывает специальный файловый объект, который хранит путь к другой цели и разрешается отдельно.
- Технические детали про конкретные файловые системы, inode internals и pathname resolution пока лучше удерживать внутри этих статей разделами, а не разносить в отдельные заметки заранее.

## Рекомендуемый маршрут чтения

1. Начать с `[[Linux File System]]` как общей Linux-specific рамки.
2. Затем прочитать `[[Linking Files]]`, чтобы зафиксировать общую картину file links.
3. После этого сопоставить `[[Hard Link]]` и `[[Symbolic Link]]`.
4. Затем возвращаться к практическим последствиям для путей, удаления файлов, перемещения и mount boundaries.

## Соседние overview-ветки

- `[[Linux File System]]`

## Что стоит раскрыть дальше

- [ ] Уточнить связь между file name, inode и directory entry
- [ ] Добавить типичные Linux cases для `ln` и `ln -s`
- [ ] Проверить `related`
- [ ] Не нужен ли рядом `pathname resolution` как отдельный узел
