---
aliases:
  - DFA
  - Детерминированный конечный автомат
note_type: article
area: computer-science
domain: algorithms
section: automata-theory
parent: "[[Finite Automaton]]"
status: draft
related:
  - "[[Finite Automaton]]"
  - "[[Nondeterministic Finite Automaton]]"
  - "[[Finite Automaton Minimization]]"
tags: []
---

# Deterministic Finite Automaton

## Краткое определение

Разновидность конечного автомата, в которой для каждого состояния и входного символа задан не более одного следующего состояния.

## Основная идея или механизм

DFA задаёт полностью определённый путь вычисления: на каждом шаге автомат однозначно знает, куда переходить по текущему символу.

## Границы темы

- В тему входит детерминированность переходов и распознавание регулярных языков.
- На границе находится `[[Nondeterministic Finite Automaton]]`, где путь вычисления уже не единственный.

## Связи с другими заметками

Родительская тема:

`[[Finite Automaton]]`

Связанные заметки:

- `[[Nondeterministic Finite Automaton]]`
- `[[Finite Automaton Minimization]]`

## Примеры, случаи или следствия

DFA особенно удобен там, где важна однозначная и эффективная обработка входной строки.

## Что стоит раскрыть дальше

- [ ] Добавить формальное определение
- [ ] Уточнить принятие строки
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
