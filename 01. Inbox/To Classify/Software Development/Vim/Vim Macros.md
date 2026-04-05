---
aliases:
  - Macros in Vim
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Vim]]"
status: seed
related:
  - "[[Vim]]"
  - "[[Vim Registers]]"
  - "[[Vim Operators]]"
  - "[[Vim Motions]]"
tags: []
---

# Vim Macros

## Краткое определение

`Vim Macros` — это статья о записи и воспроизведении последовательностей действий в Vim для повторяемого редактирования.

## Основная идея или механизм

Macro в Vim — это способ превратить ручную серию команд в воспроизводимый editing script на уровне самого редактора, без перехода к внешней автоматизации.

## Границы темы

- В тему входят запись, воспроизведение и повторное применение макросов.
- Рядом находятся `[[Vim Registers]]`, потому что запись macro хранится в register.

## Связи с другими заметками

Родительская тема:

`[[Vim]]`

Связанные заметки:

- `[[Vim Registers]]`
- `[[Vim Operators]]`
- `[[Vim Motions]]`

## Примеры, случаи или следствия

Макрос полезен там, где задача уже имеет повторяющуюся форму, но еще не требует полноценного scripting или plugin-level решения.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между macros, dot-repeat и scripting
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
