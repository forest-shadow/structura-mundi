---
aliases:
  - Agent Protocols
note_type: overview
area: computer-science
domain: artificial-intelligence
section: agent-protocols
parent: "[[AI Agent Systems]]"
status: seed
related:
  - "[[AGENTS.md]]"
  - "[[Model Context Protocol]]"
  - "[[OpenAI Codex]]"
tags: []
---

# Agent Protocols and Conventions

## Краткое определение области

`Agent Protocols and Conventions` — это обзорная ветка о повторяемых соглашениях и протоколах, через которые агентные системы получают контекст, внешние инструменты и локальные инструкции, не привязанные жестко к одной конкретной платформе.

## Что входит в эту тему

- `[[AGENTS.md]]`
- `[[Model Context Protocol]]`

## Как устроена ветка

- `AGENTS.md` описывает локальные инструкции и scoped-память проекта для агентной работы.
- `Model Context Protocol` описывает более общий интерфейс подключения внешних инструментов и источников данных.
- Ветка deliberately остается компактной: сюда входят только общие соглашения, а tool-specific реализации вынесены в `[[OpenAI Codex]]`.

## Рекомендуемый маршрут чтения

1. Начать с `[[Agent Protocols and Conventions]]`.
2. Затем прочитать `[[AGENTS.md]]` как слой локальных инструкций.
3. После этого перейти к `[[Model Context Protocol]]` как к протокольному механизму интеграции.

## Соседние overview-ветки

- Родительская рамка: `[[AI Agent Systems]]`
- Соседняя tool-specific ветка: `[[OpenAI Codex]]`

## Что стоит раскрыть дальше

- [ ] Добавить заметку про agent instruction files beyond AGENTS.md
- [ ] Добавить заметку про context injection patterns
- [ ] Проверить границы между conventions и runtime behavior
- [ ] Проверить `related`
