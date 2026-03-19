---
aliases:
  - Finite-State Machine Structure Proposal
note_type: article
area: computer-science
domain: algorithms
section: automata-theory
parent:
status: draft
related:
  - "[[Finite Automaton]]"
  - "[[Deterministic Finite Automaton]]"
  - "[[Nondeterministic Finite Automaton]]"
  - "[[Regular Language]]"
tags: []
---

# Finite Automaton Structure Proposal

## Краткое определение

Предлагаемая ветка для `Finite Automaton` оформляет конечный автомат как обзорный узел теории автоматов и связывает его с основными разновидностями и ближайшими теоретическими понятиями.

## Выбранная оптика

- `area: computer-science`
- `domain: algorithms`
- `section: automata-theory` (предлагаемое новое значение)

Почему так:

- тема естественно входит в теоретический слой computer science;
- на текущем этапе её разумно держать внутри существующего `domain: algorithms`, а не создавать отдельный новый `domain`;
- `section: automata-theory` полезен не для одной заметки, а для целой серии тем про автоматы и регулярные языки.

## Каноническое имя

- корневая заметка: `Finite Automaton`
- `Finite-State Machine`, `FSM` и `Конечный автомат` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Finite Automaton
├── Deterministic Finite Automaton
├── Nondeterministic Finite Automaton
├── Epsilon-NFA
├── Regular Language
└── Finite Automaton Minimization
```

## Почему структура именно такая

- `Finite Automaton` становится `overview`, потому что собирает под собой устойчивое семейство понятий.
- `Deterministic Finite Automaton`, `Nondeterministic Finite Automaton` и `Epsilon-NFA` — это естественные дочерние статьи по разновидностям модели.
- `Regular Language` нужен как ближайшее теоретическое соответствие: автоматы распознают именно этот класс языков.
- `Finite Automaton Minimization` нужен как отдельная статья про ключевую алгоритмическую процедуру, а не как случайная секция внутри DFA.

## Что не стоит делать сейчас

- Не нужно сразу добавлять глубокие подветки про каждую формальную деталь определения.
- Не стоит заводить отдельные заметки на уровне `state`, `alphabet` и `transition` без реальной потребности.
- Не нужно смешивать engineering-смысл `state machine` с формальной моделью без явного разграничения.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── D/
│   └── Deterministic Finite Automaton.md
├── E/
│   └── Epsilon-NFA.md
├── F/
│   ├── Finite Automaton.md
│   └── Finite Automaton Minimization.md
├── N/
│   └── Nondeterministic Finite Automaton.md
└── R/
    └── Regular Language.md
```

## Что уже создано в Inbox

- `[[Finite Automaton]]`
- `[[Deterministic Finite Automaton]]`
- `[[Nondeterministic Finite Automaton]]`
- `[[Epsilon-NFA]]`
- `[[Regular Language]]`
- `[[Finite Automaton Minimization]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между formal automata и engineering FSM
- [ ] Проверить, нужна ли отдельная статья про regex/automata equivalence
- [ ] Подтвердить `section: automata-theory`
- [ ] Проверить `related`
