---
aliases:
  - Theory of Automata Structure Proposal
note_type: article
area: computer-science
domain: algorithms
section: automata-theory
parent:
status: draft
related:
  - "[[Automata Theory]]"
  - "[[Finite Automaton]]"
  - "[[Formal Language]]"
  - "[[Chomsky Hierarchy]]"
tags: []
---

# Automata Theory Structure Proposal

## Краткое определение

Предлагаемая ветка для `Automata Theory` поднимает теорию автоматов до отдельного обзорного узла и встраивает в него уже созданную подветку `Finite Automaton`.

## Выбранная оптика

- `area: computer-science`
- `domain: algorithms`
- `section: automata-theory`

Почему так:

- тема относится к теоретическому слою computer science;
- на текущем этапе её разумно держать внутри существующего `domain: algorithms`, а не вводить новый `domain`;
- `section: automata-theory` уже оправдана не одной заметкой, а серией взаимосвязанных тем.

## Каноническое имя

- корневая заметка: `Automata Theory`
- `Theory of Automata` и `Теория автоматов` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Automata Theory
├── Formal Language
├── Chomsky Hierarchy
├── Finite Automaton
│   ├── Deterministic Finite Automaton
│   ├── Nondeterministic Finite Automaton
│   ├── Epsilon-NFA
│   ├── Regular Language
│   └── Finite Automaton Minimization
├── Pushdown Automaton
└── Turing Machine
```

## Почему структура именно такая

- `Automata Theory` должен быть `overview`, потому что собирает несколько устойчивых классов моделей и языков.
- `Finite Automaton` уже оправдан как дочерний `sub-overview`, поскольку у него есть собственная плотная ветка.
- `Formal Language`, `Pushdown Automaton`, `Turing Machine` и `Chomsky Hierarchy` пока лучше оставить обычными `article`, чтобы не делать вложенность глубже без корпуса заметок.

## Что не стоит делать сейчас

- Не стоит сразу строить отдельные подветки под каждый класс грамматик.
- Не стоит смешивать formal-language perspective с engineering-смыслом state machines без явного разграничения.
- Не стоит создавать ещё один уровень overview между `Automata Theory` и `Finite Automaton`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── A/
│   └── Automata Theory.md
├── C/
│   └── Chomsky Hierarchy.md
├── D/
│   └── Deterministic Finite Automaton.md
├── E/
│   └── Epsilon-NFA.md
├── F/
│   ├── Finite Automaton.md
│   ├── Finite Automaton Minimization.md
│   └── Formal Language.md
├── N/
│   └── Nondeterministic Finite Automaton.md
├── P/
│   └── Pushdown Automaton.md
├── R/
│   └── Regular Language.md
└── T/
    └── Turing Machine.md
```

## Что уже создано в Inbox

- `[[Automata Theory]]`
- `[[Formal Language]]`
- `[[Chomsky Hierarchy]]`
- `[[Finite Automaton]]`
- `[[Deterministic Finite Automaton]]`
- `[[Nondeterministic Finite Automaton]]`
- `[[Epsilon-NFA]]`
- `[[Regular Language]]`
- `[[Finite Automaton Minimization]]`
- `[[Pushdown Automaton]]`
- `[[Turing Machine]]`

## Что стоит раскрыть дальше

- [ ] Уточнить место grammar-центричных тем рядом с automata theory
- [ ] Проверить, нужен ли отдельный article про regex/automata equivalence
- [ ] Подтвердить `section: automata-theory`
- [ ] Проверить `related`
