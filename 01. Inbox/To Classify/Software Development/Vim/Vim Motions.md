---
aliases:
  - Navigation in Vim
note_type: article
area: computer-science
domain: software-development
section: vim
parent: "[[Vim Commands]]"
status: seed
related:
  - "[[Vim Commands]]"
  - "[[Vim]]"
  - "[[Vim Modes]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
tags: []
---
![[01. Inbox/To Classify/Software Development/Vim/_resources/2ccba2a570b0f6a58a3e4964bd2b3888_MD5.jpg]]
# Vim Motions

## Краткое определение

`Vim Motions` — это статья о командах перемещения в Vim, которые задают navigation language и одновременно используются как строительные блоки для редактирования.

## Основная идея или механизм

Motion в Vim — это не просто способ сдвинуть курсор, а структурная единица, которую можно комбинировать с operators для выражения редактирующего действия.

## Границы темы

- В тему входят перемещения по символам, словам, строкам, предложениям, абзацам и экрану.
- Рядом находятся `[[Vim Operators]]` и `[[Vim Text Objects]]`, потому что именно с ними motions образуют editing language.

## Связи с другими заметками

Родительская тема:

`[[Vim Commands]]`

Связанные заметки:

- `[[Vim Modes]]`
- `[[Vim]]`
- `[[Vim Operators]]`
- `[[Vim Text Objects]]`

## Примеры, случаи или следствия

Команда вроде `dw` работает именно потому, что `d` — operator, а `w` — motion. Это показывает, что navigation в Vim сразу встроена в модель редактирования.

## Что стоит раскрыть дальше

- [ ] Добавить карту базовых motions по уровням текста
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
