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
  - "[[Vim Commands]]"
  - "[[Vim Modes]]"
  - "[[Vim Motions]]"
  - "[[Vim Operators]]"
  - "[[Vim Text Objects]]"
  - "[[Vim Registers]]"
tags: []
---

# Vim

## Краткое определение области

`Vim` — это обзорная заметка о текстовом редакторе Vim как о системе modal editing, внутри которой естественно собираются modes, commands, registers, macros и модель работы с buffers, windows и tabs.

## Что входит в эту тему

- `[[Vim Modes]]`
- `[[Vim Commands]]`
- `[[Vim Registers]]`
- `[[Vim Macros]]`
- `[[Vim Buffers, Windows, and Tabs]]`

## Как устроена ветка

- `Vim` служит tool-overview узлом и не должен сам пытаться до конца раскрыть каждую команду и каждый режим.
- `Vim Modes` удерживают базовую modal model редактора, внутри которой отдельным дочерним понятием позже раскрывается `Vim Command-line Mode`.
- `Vim Commands` собирают command-centric слой редактора: motions, operators, text objects и `Ex`-команды.
- `Vim Registers` и `Vim Macros` описывают механизмы повторного использования текста и действий.
- `Vim Buffers, Windows, and Tabs` удерживают рабочую модель навигации по файлам и раскладкам.

## Рекомендуемый маршрут чтения

1. Начать с `[[Vim Modes]]`.
2. Затем перейти к `[[Vim Commands]]`.
3. После этого читать `[[Vim Registers]]` и `[[Vim Macros]]`.
4. Завершить `[[Vim Buffers, Windows, and Tabs]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Software Development]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `Vim Commands` нужен отдельный узел про search/replace workflows
- [ ] Проверить, нужен ли позже отдельный узел про Vim configuration
- [ ] Проверить, когда buffers/windows/tabs стоит разнести на отдельные notes
- [ ] Проверить `related`
