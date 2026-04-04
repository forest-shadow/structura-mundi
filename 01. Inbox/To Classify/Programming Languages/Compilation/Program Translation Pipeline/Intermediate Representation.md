---
aliases:
  - IR
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Translation Pipeline]]"
status: seed
related:
  - "[[Semantic Analysis]]"
  - "[[Code Generation]]"
  - "[[Program Translation Pipeline]]"
tags: []
---

# Intermediate Representation

## Краткое определение

`Intermediate Representation` — это внутреннее представление программы, расположенное между высокоуровневой синтаксической формой и конечным машинным кодом.

## Основная идея или механизм

IR нужен, чтобы отделить front-end стадии анализа языка от back-end стадий optimization и code generation, сделав compiler architecture более управляемой и переносимой.

## Границы темы

- Входит: роль IR как промежуточного слоя, связь с lowering и optimization.
- Не входит: исходная surface syntax языка и итоговый executable artifact как таковой.

## Связи с другими заметками

Родительская тема:

`[[Program Translation Pipeline]]`

Связанные заметки:

- `[[Semantic Analysis]]`
- `[[Code Generation]]`
- `[[Program Translation Pipeline]]`

## Примеры, случаи или следствия

Один и тот же front-end может понижать программу в IR, после чего разные back-end компоненты уже генерируют код под разные архитектуры.

## Что стоит раскрыть дальше

- [ ] Уточнить различие high-level IR и low-level IR
- [ ] Проверить, когда нужны отдельные notes про SSA и CFG
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
