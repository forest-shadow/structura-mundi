---
aliases:
  - Compilation Pipeline
  - Source Code Compilation Pipeline
  - Source Code Translation Pipeline
note_type: overview
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Compilation]]"
  - "[[Abstract Syntax Tree]]"
  - "[[Machine Code]]"
  - "[[Object File]]"
  - "[[Shared Library]]"
  - "[[Executable Binary]]"
tags: []
---

# Program Translation Pipeline

## Краткое определение области

`Program Translation Pipeline` — это обзорная заметка о типовой последовательности стадий, через которые проходит программа при движении от исходного кода к низкоуровневым представлениям и итоговому исполнимому артефакту.

## Что входит в эту тему

- `[[Lexical Analysis]]`
- `[[Parsing]]`
- `[[Semantic Analysis]]`
- `[[Intermediate Representation]]`
- `[[Code Generation]]`
- `[[Linking]]`

## Как устроена ветка

- Эта ветка собирает именно стадии и переходы процесса.
- Представления и артефакты вроде `[[Abstract Syntax Tree]]`, `[[Machine Code]]`, `[[Object File]]`, `[[Shared Library]]` и `[[Executable Binary]]` остаются рядом как отдельные статьи, потому что на них ссылаются сразу несколько стадий pipeline.
- В каноническом имени не используется слово execution, потому что эта заметка про translation/build flow, а не про runtime behavior уже запущенной программы.

## Соседние overview-ветки

- `[[Compilation]]`

## Рекомендуемый маршрут чтения

1. Начать с `Program Translation Pipeline`.
2. Затем пройти по стадиям от `[[Lexical Analysis]]` и `[[Parsing]]` к `[[Semantic Analysis]]`.
3. После этого читать `[[Intermediate Representation]]`, `[[Code Generation]]` и `[[Linking]]`.
4. Параллельно сверяться с `[[Abstract Syntax Tree]]`, `[[Machine Code]]`, `[[Object File]]`, `[[Shared Library]]` и `[[Executable Binary]]` как с ключевыми представлениями и результатами.

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужен отдельный узел про optimization pipeline
- [ ] Проверить, нужен ли рядом отдельный узел про assembly
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
