---
aliases:
  - ε-NFA
  - Epsilon NFA
  - Автомат с эпсилон-переходами
note_type: article
area: computer-science
domain: algorithms
section: automata-theory
parent: "[[Finite Automaton]]"
status: draft
related:
  - "[[Finite Automaton]]"
  - "[[Nondeterministic Finite Automaton]]"
  - "[[Regular Language]]"
tags: []
---

# Epsilon-NFA

## Краткое определение

Разновидность NFA, допускающая переходы без чтения входного символа.

## Основная идея или механизм

Эпсилон-переходы позволяют автомату менять состояние без потребления символа, что делает описание некоторых конструкций более удобным.

## Границы темы

- В тему входят пустые переходы и их влияние на построение автомата.
- На границе находится обычный `[[Nondeterministic Finite Automaton]]`, где все переходы привязаны к входным символам.

## Связи с другими заметками

Родительская тема:

`[[Finite Automaton]]`

Связанные заметки:

- `[[Nondeterministic Finite Automaton]]`
- `[[Regular Language]]`

## Примеры, случаи или следствия

Эпсилон-переходы часто возникают при построении автомата из регулярного выражения.

## Что стоит раскрыть дальше

- [ ] Добавить epsilon-closure
- [ ] Уточнить роль в преобразованиях автомата
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
