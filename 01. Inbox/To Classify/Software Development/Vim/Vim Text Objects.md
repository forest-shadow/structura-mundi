---
aliases:
  - Text Objects in Vim
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Vim Commands]]"
status: seed
related:
  - "[[Vim Commands]]"
  - "[[Vim]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Modes]]"
tags: []
---

# Vim Text Objects

## Краткое определение

`Vim Text Objects` — это статья о структурных единицах текста в Vim, к которым можно применять operators без ручного выделения символов по одному.

## Основная идея или механизм

Text objects позволяют редактировать не позицию курсора саму по себе, а уже осмысленную текстовую сущность: слово, абзац, кавычки, скобки и другие структурные границы.

## Границы темы

- В тему входят `inner` и `around`-объекты и их связь с operators.
- Рядом находятся `[[Vim Motions]]`, но motions описывают перемещение, а не выбор структурного объекта.

## Связи с другими заметками

Родительская тема:

`[[Vim Commands]]`

Связанные заметки:

- `[[Vim Motions]]`
- `[[Vim Operators]]`
- `[[Vim]]`
- `[[Vim Modes]]`

## Примеры, случаи или следствия

Команды вроде `ci(` или `da"` показывают, что Vim умеет мыслить объектами текста, а не только линейными перемещениями.

## Что стоит раскрыть дальше

- [ ] Добавить карту базовых text objects
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
