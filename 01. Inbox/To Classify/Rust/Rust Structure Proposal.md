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
  - "[[Rust Trait]]"
  - "[[Rust Crate]]"
tags: []
---

# Rust Structure Proposal

## Краткое определение

Предлагаемая ветка для `Rust` задает минимальную, но устойчивую иерархию заметок о языке, в которую уже естественно помещаются понятия `trait` и `crate`, без преждевременного введения лишних подветок.

## Выбранная оптика

- `area: computer-science`
- `domain: programming-languages`
- `section: rust` (предлагаемое новое значение)

Почему так:

- `Rust` естественно живет внутри уже существующего `domain: programming-languages`;
- тема не требует нового `domain`, потому что речь идет о языковой ветке, а не об отдельной дисциплине;
- `section: rust` оправдан не одной заметкой, а как минимум серией взаимосвязанных language-notes про сам язык, его типовую модель и организацию кода.

## Каноническое имя

- корневая обзорная заметка: `Rust`
- понятие `trait` лучше хранить как `Rust Trait`, чтобы не терять языковой контекст
- понятие `crate` лучше хранить как `Rust Crate`, потому что вне Rust этот термин недостаточно самодостаточен

## Рекомендуемая иерархия

```text
Rust
├── Rust Trait
└── Rust Crate
```

## Почему структура именно такая

- `Rust` должен быть корневым `overview`, потому что собирает под одной рамкой базовые узлы языка.
- `Rust Trait` на текущем этапе лучше держать обычной `article`, а не отдельным `sub-overview`: одного понятия пока недостаточно, чтобы оправдать дополнительный уровень вложенности.
- `Rust Crate` тоже лучше держать обычной `article`, потому что минимальная ветка пока должна оставаться плоской: `root overview -> article`.
- `trait` и `crate` принадлежат разным смысловым слоям языка, но это не требует немедленно разводить их по разным sub-overview, пока корпус еще компактен.
- Когда рядом появятся заметки вроде `Rust Trait Bounds`, `Rust Trait Objects`, `Rust Associated Types`, `Rust Modules`, `Cargo Package` или `Rust Visibility`, тогда уже можно будет поднимать отдельные подветки.

## Что не стоит делать прямо сейчас

- Не стоит заранее вводить `Rust Type System` только ради одной заметки `Rust Trait`.
- Не стоит заранее вводить `Rust Package Model` только ради одной заметки `Rust Crate`.
- Не стоит смешивать `crate`, `package`, `module` и `workspace` в одной заметке как будто это синонимы.
- Не стоит создавать специальные `Rust`-templates: по правилам `Principia Rerum` здесь достаточно канонических `overview/article`.

## Предлагаемое физическое размещение после нормализации

```text
02. Corpus Mundi/
├── R/
│   ├── Rust.md
│   └── Rust Crate.md
└── T/
    └── Rust Trait.md
```

Логическая ветка при этом все равно собирается через `parent`, а не через соседство файлов.

## Что уже создано в Inbox

- `[[Rust]]`
- `[[Rust Trait]]`
- `[[Rust Crate]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: rust`
- [ ] Проверить, когда `Rust Trait` вырастает в отдельную sub-overview-ветку
- [ ] Проверить, когда рядом с `Rust Crate` нужны `Cargo Package`, `Rust Module` и `Rust Visibility`
- [ ] Проверить `related`
