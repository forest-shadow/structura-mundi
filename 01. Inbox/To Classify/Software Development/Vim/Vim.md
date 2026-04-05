---
aliases:
  - Vim Editor
  - Вим
note_type: overview
area: computer-science
domain: software-development
section: vim
parent: "[[Software Development]]"
status: seed
related:
  - "[[Software Development]]"
  - "[[Vim Modes]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
  - "[[Vim Registers]]"
tags: []
---

# Vim

## Краткое определение области

`Vim` — это обзорная заметка о текстовом редакторе Vim как о системе modal editing, внутри которой естественно собираются modes, motions, operators, text objects, registers, macros и модель работы с buffers, windows и tabs.

## Что входит в эту тему

- `[[Vim Modes]]`
- `[[Vim Motions]]`
- `[[Vim Operators]]`
- `[[Vim Text Objects]]`
- `[[Vim Registers]]`
- `[[Vim Macros]]`
- `[[Vim Buffers, Windows, and Tabs]]`

## Как устроена ветка

- `Vim` служит tool-overview узлом и не должен сам пытаться до конца раскрыть каждую команду и каждый режим.
- `Vim Modes` удерживают базовую modal model редактора.
- `Vim Motions`, `Vim Operators` и `Vim Text Objects` собирают ядро editing language.
- `Vim Registers` и `Vim Macros` описывают механизмы повторного использования текста и действий.
- `Vim Buffers, Windows, and Tabs` удерживают рабочую модель навигации по файлам и раскладкам.

## Рекомендуемый маршрут чтения

1. Начать с `[[Vim Modes]]`.
2. Затем перейти к `[[Vim Motions]]` и `[[Vim Operators]]`.
3. После этого читать `[[Vim Text Objects]]` и `[[Vim Registers]]`.
4. Завершить `[[Vim Macros]]` и `[[Vim Buffers, Windows, and Tabs]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Software Development]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли позже отдельный узел про Vim configuration
- [ ] Проверить, когда buffers/windows/tabs стоит разнести на отдельные notes
- [ ] Проверить `related`
