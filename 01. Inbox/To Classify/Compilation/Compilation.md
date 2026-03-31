---
aliases: []
note_type: overview
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Programming Languages]]"
status: seed
related:
  - "[[Programming Languages]]"
  - "[[Program Translation Pipeline]]"
  - "[[Abstract Syntax Tree]]"
  - "[[Machine Code]]"
  - "[[Executable Binary]]"
tags: []
---

# Compilation

## Краткое определение области

`Compilation` — это обзорная заметка для ветки о преобразовании исходного кода в более низкоуровневые представления и итоговые исполнимые артефакты.

## Что входит в эту тему

- `[[Program Translation Pipeline]]`
- `[[Abstract Syntax Tree]]`
- `[[Machine Code]]`
- `[[Executable Binary]]`

## Как устроена ветка

- `Compilation` служит корневым `overview` для общей темы трансляции программы.
- Отдельный вложенный `overview` `[[Program Translation Pipeline]]` нужен для устойчивого набора стадий вроде lexical analysis, parsing, semantic analysis, code generation и linking.
- `Abstract Syntax Tree`, `Machine Code` и `Executable Binary` лучше держать отдельными `article`, потому что это не просто шаги конвейера, а самостоятельные представления или артефакты, к которым будут вести ссылки из разных частей ветки.

## Соседние overview-ветки

- Родительская рамка: `[[Programming Languages]]`

## Рекомендуемый маршрут чтения

1. Начать с `Compilation`.
2. Затем перейти к `[[Program Translation Pipeline]]`, чтобы увидеть общую последовательность преобразований.
3. После этого читать `[[Abstract Syntax Tree]]`, `[[Machine Code]]` и `[[Executable Binary]]` как ключевые представления и результаты процесса.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Compiler`, `Interpreter` и `Linker`
- [ ] Проверить границы между compilation, build pipeline и program execution
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
