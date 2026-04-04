---
aliases:
  - Lexing
  - Tokenization in Compilation
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Translation Pipeline]]"
status: seed
related:
  - "[[Parsing]]"
  - "[[Program Translation Pipeline]]"
tags: []
---

# Lexical Analysis

## Краткое определение

`Lexical Analysis` — это стадия, на которой исходный текст программы разбивается на токены, пригодные для дальнейшего синтаксического разбора.

## Основная идея или механизм

Лексический анализ превращает поток символов в более структурированный поток лексем: идентификаторы, ключевые слова, литералы, операторы и разделители.

## Границы темы

- Входит: токены, лексемы, роль lexer между source text и parser.
- Не входит: построение дерева программы и семантическая проверка.

## Связи с другими заметками

Родительская тема:

`[[Program Translation Pipeline]]`

Связанные заметки:

- `[[Parsing]]`
- `[[Program Translation Pipeline]]`

## Примеры, случаи или следствия

До lexical analysis последовательность `if (x + 1)` является просто текстом; после него она уже представлена как последовательность токенов, с которой может работать parser.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между token, lexeme и grammar terminal
- [ ] Проверить связь с regular languages и automata theory
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
