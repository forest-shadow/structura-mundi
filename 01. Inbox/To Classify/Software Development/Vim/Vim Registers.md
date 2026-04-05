---
aliases:
  - Registers in Vim
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Vim]]"
status: seed
related:
  - "[[Vim]]"
  - "[[Vim Operators]]"
  - "[[Vim Macros]]"
  - "[[Vim Modes]]"
tags: []
---

# Vim Registers

## Краткое определение

`Vim Registers` — это статья о буферах хранения текста и команд в Vim, через которые работают yank, delete, paste, macros и named registers.

## Основная идея или механизм

Registers делают редактирование в Vim не только мгновенным, но и накопительным: текст и действия можно сохранять, адресовать по имени и повторно использовать.

## Границы темы

- В тему входят unnamed, numbered, named и special registers.
- Рядом находятся `[[Vim Macros]]`, потому что macros тоже используют registers как носитель записи действий.

## Связи с другими заметками

Родительская тема:

`[[Vim]]`

Связанные заметки:

- `[[Vim Operators]]`
- `[[Vim Macros]]`
- `[[Vim Modes]]`

## Примеры, случаи или следствия

Понимание registers объясняет, почему удаление и копирование в Vim ведут себя не как простая замена системного clipboard, а как более богатая модель хранения текста.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между unnamed, numbered, named и clipboard registers
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
