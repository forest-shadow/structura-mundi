---
aliases:
  - Modal Editing in Vim
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Vim]]"
status: seed
related:
  - "[[Vim]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
tags: []
---
![[01. Inbox/To Classify/Software Development/Vim/_resources/383ecf39b6738051004503a0e8ba6e74_MD5.jpg]]
# Vim Modes

## Краткое определение

`Vim Modes` — это статья о режимах Vim как о базовой modal model редактора: normal, insert, visual, select, command-line и других рабочих состояниях.

## Основная идея или механизм

В Vim одна и та же клавиатура получает разный смысл в зависимости от текущего режима. Именно поэтому modes задают фундамент всей ветки: без них трудно понять motions, operators и команды редактирования.

## Границы темы

- В тему входят основные режимы и переходы между ними.
- Рядом находятся `[[Vim Motions]]` и `[[Vim Operators]]`, но они уже описывают действия внутри modal model.

## Связи с другими заметками

Родительская тема:

`[[Vim]]`

Связанные заметки:

- `[[Vim Motions]]`
- `[[Vim Operators]]`
- `[[Vim Text Objects]]`

## Примеры, случаи или следствия

Понимание normal mode как базового состояния меняет способ работы с редактором: ввод текста перестает быть default-режимом, а редактирование становится набором команд.

## Что стоит раскрыть дальше

- [ ] Уточнить роль normal, insert, visual и command-line modes
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
