---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: file-systems
parent: "[[Operating Systems]]"
status: seed
related:
  - "[[System Calls]]"
  - "[[Linux File System]]"
tags: []
---

# File Systems

## Краткое определение

`File Systems` — это заметка про механизм организации и именования долговременного хранения данных, с которым операционная система работает как с логической структурой файлов и каталогов.

## Почему тема находится в ветке Operating Systems

Эта тема относится к корневой OS-ветке, потому что файловая система — это отдельный базовый subsystem, а не частный аспект execution model или virtual memory.

## Основная идея или механизм

- ОС предоставляет логическую модель файлов, директорий и путей;
- эта модель скрывает детали физического размещения данных;
- приложения взаимодействуют с ней через системные вызовы и файловые операции.

## Границы темы

- Входит: file system как OS abstraction for persistent storage.
- Не входит: полный разбор journaling, inode layouts и всех конкретных file system implementations.
- Linux-specific устройство файловой подсистемы лучше раскрывать отдельно в `[[Linux File System]]`, а не перегружать эту общую заметку деталями одной OS-ветки.

## Примеры, случаи или следствия

Эта заметка должна показать, почему persistent storage в ОС организуется не как "сырые блоки", а как управляемая и адресуемая логическая структура.

## Связи с другими заметками

Родительская тема:

`[[Operating Systems]]`

Связанные заметки:

- `[[System Calls]]`
- `[[Linux File System]]`

## Что стоит раскрыть дальше

- [ ] Развести file abstraction и storage device details
- [ ] Добавить связь с path namespace и directories
- [ ] Проверить границу между общей статьей `File Systems` и Linux-specific заметкой `Linux File System`
- [ ] Проверить `related`
- [ ] Проверить `aliases`