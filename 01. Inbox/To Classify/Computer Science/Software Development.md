---
aliases:
  - Разработка программного обеспечения
  - Developer Tooling
note_type: overview
area: computer-science
domain: software-development
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Computer Science]]"
  - "[[Programming Languages]]"
  - "[[Software Architecture]]"
  - "[[Vim]]"
tags: []
---

# Software Development

## Краткое определение области

`Software Development` — это domain-root overview для заметок об инструментах, практиках и рабочих средах разработки программного обеспечения: редакторах, version control, build tooling, testing tooling и других инженерных механизмах, через которые разработчик работает с кодом.

## Что входит в эту тему

- `[[Vim]]`

## Как устроена ветка

- `Software Development` собирает не теорию архитектуры и не семантику языков, а именно инструментальный и workflow-слой разработки.
- `Vim` оправдан как первый section-level overview внутри этого домена, потому что вокруг него уже естественно выделяются modes, motions, operators, text objects, registers, macros и рабочая модель окон и буферов.
- `Software Architecture` остается соседним доменом, потому что описывает организацию системы, а не инструменты редактирования и разработки.
- `Programming Languages` остается соседним доменом, потому что описывает языки и модели выполнения, а не editor-specific практики.

## Рекомендуемый маршрут чтения

1. Начать с `[[Vim]]` как первой плотной tool-ветки в домене.
2. Затем перейти к `[[Vim Modes]]` и `[[Vim Motions]]`.
3. После этого читать `[[Vim Operators]]`, `[[Vim Text Objects]]` и `[[Vim Registers]]`.
4. Завершить `[[Vim Macros]]` и `[[Vim Buffers, Windows, and Tabs]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`
- Соседние домены: `[[Programming Languages]]`, `[[Software Architecture]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `Vim` нужны `Git` и build-tooling notes
- [ ] Проверить границу между software development tooling и language-specific toolchains
- [ ] Проверить `related`
