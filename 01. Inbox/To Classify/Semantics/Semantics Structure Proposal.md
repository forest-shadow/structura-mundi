---
aliases:
  - Семантика
note_type: article
area: linguistics
domain: linguistic-theory
section: semantics
parent:
status: draft
related:
  - "[[Semantics]]"
  - "[[Lexical Semantics]]"
  - "[[Formal Semantics]]"
  - "[[Semantics and Pragmatics]]"
tags: []
---

# Semantics Structure Proposal

## Краткое определение

Предлагаемая ветка для `Semantics` описывает семантику как самостоятельную область внутри лингвистической теории, связанную с вопросами значения, денотации, композиционности и границы с прагматикой.

## Выбранная оптика

- `area: linguistics`
- `domain: linguistic-theory` (предлагаемое новое значение)
- `section: semantics` (предлагаемое новое значение)

Почему так:

- тема слишком широка, чтобы оставаться без явной дисциплинарной оптики;
- `linguistics` уже есть как `area`, а `Semantics` естественно вписывается в неё как поддисциплина;
- `domain: linguistic-theory` полезен не только для одной заметки, но и для будущих веток о syntax, pragmatics, phonology и других теоретических темах;
- `section: semantics` позволяет собрать плотный тематический кластер внутри этого домена.

## Почему не стоит делать ветку глубже прямо сейчас

- `Semantics` действительно допускает сложную иерархию, но на текущем шаге достаточно одного обзорного узла и плоского набора ключевых статей.
- Дополнительные `sub-overview` вроде `Lexical Semantics` или `Formal Semantics` можно будет ввести позже, если по ним появится самостоятельная плотная серия заметок.
- Это соответствует правилу минимальной вложенности в `Principia Rerum`.

## Предлагаемая логическая структура

```text
Semantics
├── Linguistic Meaning
├── Denotation
├── Sense and Reference
├── Lexical Semantics
├── Compositional Semantics
├── Formal Semantics
└── Semantics and Pragmatics
```

## Роли заметок

- `[[Semantics]]` — корневой `overview`
- `[[Linguistic Meaning]]` — базовая статья о значении как центральном объекте семантики
- `[[Denotation]]` — статья о соотнесении выражений с объектами, классами объектов или условиями истинности
- `[[Sense and Reference]]` — статья о классическом различении смысла и референции
- `[[Lexical Semantics]]` — статья о значении слов и лексических единиц
- `[[Compositional Semantics]]` — статья о том, как значение сложных выражений строится из значений частей
- `[[Formal Semantics]]` — статья о логико-модельном аппарате описания значения
- `[[Semantics and Pragmatics]]` — статья о границе между кодированным значением и контекстуальным выводом

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── C/
│   └── Compositional Semantics.md
├── D/
│   └── Denotation.md
├── F/
│   └── Formal Semantics.md
├── L/
│   ├── Lexical Semantics.md
│   └── Linguistic Meaning.md
├── S/
│   ├── Semantics.md
│   ├── Semantics and Pragmatics.md
│   └── Sense and Reference.md
```

## Что уже создано в Inbox

- `[[Semantics]]`
- `[[Linguistic Meaning]]`
- `[[Denotation]]`
- `[[Sense and Reference]]`
- `[[Lexical Semantics]]`
- `[[Compositional Semantics]]`
- `[[Formal Semantics]]`
- `[[Semantics and Pragmatics]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, нужна ли в этой ветке отдельная заметка `Reference`
- [ ] Решить, когда `Lexical Semantics` стоит повышать до `overview`
- [ ] Добавить соседние связи с будущими ветками `Syntax` и `Pragmatics`
- [ ] Подтвердить `domain: linguistic-theory`
- [ ] Подтвердить `section: semantics`
