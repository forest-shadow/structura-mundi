---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: rust
parent: "[[Programming Languages]]"
status: draft
related:
  - "[[Programming Languages]]"
  - "[[Rust]]"
  - "[[Rust Ownership]]"
  - "[[Rust Traits]]"
  - "[[Rust Cargo and Toolchain]]"
tags: []
---

# Rust Structure Proposal

## Краткое определение

Предлагаемая ветка для `Rust` разворачивает язык в устойчивую учебно-смысловую иерархию заметок, где ownership-ветка получает локальную вложенность, а темы вроде traits, pattern matching, unsafe и toolchain остаются самостоятельными узлами верхнего слоя.

## Выбранная оптика

- `area: computer-science`
- `domain: programming-languages`
- `section: rust` (предлагаемое новое значение)

Почему так:

- `Rust` естественно живет внутри уже существующего `domain: programming-languages`;
- тема не требует нового `domain`, потому что речь идет о языковой ветке, а не об отдельной дисциплине;
- `section: rust` оправдан уже не одной заметкой, а серией взаимосвязанных language-notes про владение памятью, абстракции, algebraic data types, unsafe-код и организацию проекта.

## Каноническое имя

- корневая обзорная заметка: `Rust`
- ownership-ветку лучше именовать через `Rust Ownership`, `Rust Borrowing`, `Rust Lifetimes`
- заметку про traits лучше хранить как `Rust Traits`, чтобы не терять языковой контекст
- заметку про crate лучше хранить как `Rust Crate`, а держать ее внутри ветки `Rust Cargo and Toolchain`

## Рекомендуемая иерархия

```text
Rust
├── Rust Ownership
│   └── Rust Borrowing
│       └── Rust Lifetimes
├── Rust Traits
├── Rust Enums and Pattern Matching
├── Unsafe Rust
└── Rust Cargo and Toolchain
    └── Rust Crate
```

## Почему структура именно такая

- `Rust` должен быть корневым `overview`, потому что собирает под одной рамкой несколько самостоятельных тематических кластеров языка.
- `Rust Ownership` уже оправдан как дочерний `overview`, потому что под ним естественно группируются `Rust Borrowing` и `Rust Lifetimes`.
- `Rust Borrowing` тоже оправдан как локальный `overview`, потому что lifetimes в Rust обычно раскрываются как механизм, уточняющий правила заимствования, а не как полностью изолированная тема.
- `Rust Traits`, `Rust Enums and Pattern Matching` и `Unsafe Rust` пока лучше оставлять обычными `article`, чтобы не плодить лишние уровни вложенности без плотного корпуса дочерних заметок.
- `Rust Cargo and Toolchain` оправдан как отдельный `overview`, потому что здесь уже есть по меньшей мере один устойчивый дочерний узел `Rust Crate`, а позже сюда же естественно добавляются `Cargo Package`, `Rust Modules`, `Cargo.toml`, `Rust Workspace` и связанные toolchain-notes.
- Последовательность `Rust Ownership -> Rust Borrowing -> Rust Lifetimes -> Rust Traits -> Rust Enums and Pattern Matching -> Unsafe Rust -> Rust Cargo and Toolchain` лучше понимать как рекомендуемый маршрут чтения, а не как жесткую цепочку `parent`, потому что по `Principia Rerum` иерархия должна оставаться смысловой, а не просто линейно-учебной.

## Что не стоит делать прямо сейчас

- Не стоит заранее вводить `Rust Type System` только ради одной заметки `Rust Traits`.
- Не стоит смешивать `crate`, `package`, `module` и `workspace` в одной заметке как будто это синонимы.
- Не стоит выстраивать `Traits -> Enums and Pattern Matching -> Unsafe Rust` через `parent` только ради следования учебной последовательности.
- Не стоит создавать специальные `Rust`-templates: по правилам `Principia Rerum` здесь достаточно канонических `overview/article`.

## Предлагаемое физическое размещение после нормализации

```text
01. Inbox/To Classify/Rust/
├── Rust.md
├── Rust Structure Proposal.md
├── Rust Ownership/
│   ├── Rust Ownership.md
│   └── Rust Borrowing/
│       ├── Rust Borrowing.md
│       └── Rust Lifetimes.md
├── Rust Traits.md
├── Rust Enums and Pattern Matching.md
├── Unsafe Rust.md
└── Rust Cargo and Toolchain/
    ├── Rust Cargo and Toolchain.md
    └── Rust Crate.md
```

После переноса в `Corpus Mundi` физическое размещение снова должно стать алфавитным, а логическая ветка по-прежнему будет собираться через `parent`.

## Что уже создано в Inbox

- `[[Rust]]`
- `[[Rust Ownership]]`
- `[[Rust Borrowing]]`
- `[[Rust Lifetimes]]`
- `[[Rust Traits]]`
- `[[Rust Enums and Pattern Matching]]`
- `[[Unsafe Rust]]`
- `[[Rust Cargo and Toolchain]]`
- `[[Rust Crate]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: rust`
- [ ] Проверить, когда рядом с `Rust Traits` нужны `Rust Trait Bounds`, `Rust Trait Objects` и `Rust Associated Types`
- [ ] Проверить, когда `Rust Enums and Pattern Matching` стоит разделить на две отдельные notes
- [ ] Проверить, когда рядом с `Rust Cargo and Toolchain` нужны `Cargo Package`, `Rust Module`, `Cargo.toml` и `Rust Workspace`
- [ ] Проверить `related`


# Rust: Рекомендуемый маршрут чтения

1. Начать с `Rust`.
2. Затем перейти к `[[Rust Ownership]]`.
3. После этого читать `[[Rust Borrowing]]` и `[[Rust Lifetimes]]`.
4. Затем перейти к `[[Rust Traits]]`.
5. После этого читать `[[Rust Enums and Pattern Matching]]`.
6. Затем перейти к `[[Unsafe Rust]]`.
7. Завершить веткой `[[Rust Cargo and Toolchain]]` и дочерней заметкой `[[Rust Crate]]`.