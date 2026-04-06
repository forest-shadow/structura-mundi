---
aliases:
  - Vim Command Language
note_type: overview
area: computer-science
domain: software-development
section: vim
parent: "[[Vim]]"
status: seed
related:
  - "[[Vim]]"
  - "[[Vim Modes]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
  - "[[Vim Ex Commands]]"
tags: []
---

# Vim Commands

## Краткое определение области

`Vim Commands` — это обзорная заметка о командной грамматике Vim: о тех семействах действий, через которые редактор описывает перемещение, редактирование, работу со структурными объектами текста и вызов `Ex`-команд.

## Что входит в эту тему

- `[[Vim Motions]]`
- `[[Vim Operators]]`
- `[[Vim Text Objects]]`
- `[[Vim Ex Commands]]`

## Как устроена ветка

- `Vim Commands` собирает не все аспекты Vim подряд, а именно command-centric слой редактора.
- `Vim Motions` задают пространство перемещения и область действия для других команд.
- `Vim Operators` описывают преобразующие действия над текстом.
- `Vim Text Objects` добавляют структурный способ адресовать фрагменты текста.
- `Vim Ex Commands` покрывают линейку `:`-команд, которые работают через command-line интерфейс редактора.
- `Vim Command-line Mode` остается связанной, но соседней темой, потому что это mode-level рамка для ввода части этих команд, а не отдельное семейство команд само по себе.

## Рекомендуемый маршрут чтения

1. Начать с `[[Vim Motions]]`.
2. Затем перейти к `[[Vim Operators]]`.
3. После этого читать `[[Vim Text Objects]]`.
4. Завершить `[[Vim Ex Commands]]`, а затем при необходимости вернуться к `[[Vim Command-line Mode]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Vim]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда `Vim Ex Commands` пора поднимать до отдельного sub-overview
- [ ] Проверить, нужны ли отдельные статьи про ranges, substitute и global-команды
- [ ] Проверить `related`
