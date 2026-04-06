---
aliases:
  - Editing Operators in Vim
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
  - "[[Vim Text Objects]]"
  - "[[Vim Registers]]"
tags: []
---

# Vim Operators

## Краткое определение

`Vim Operators` — это статья о командах редактирования в Vim, которые применяются к motion или text object и задают основную editing grammar редактора.

## Основная идея или механизм

Operators вроде delete, change и yank получают полный смысл только в комбинации с motion или text object. Поэтому редактирование в Vim строится как композиция, а не как набор изолированных shortcuts.

## Границы темы

- В тему входят базовые операторы и их сочетание с motions и text objects.
- Рядом находятся `[[Vim Registers]]`, но она уже описывает хранение текста и историю операций.

## Связи с другими заметками

Родительская тема:

`[[Vim Commands]]`

Связанные заметки:

- `[[Vim Motions]]`
- `[[Vim Text Objects]]`
- `[[Vim]]`
- `[[Vim Registers]]`

## Примеры, случаи или следствия

Связка вроде `ciw` показывает, что оператор может быть направлен не только на движение, но и на структурный объект текста.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между delete, change, yank и format-like operators
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
