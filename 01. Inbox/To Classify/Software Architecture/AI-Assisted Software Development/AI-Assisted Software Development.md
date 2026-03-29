---
aliases:
  - Agentic Software Engineering
note_type: overview
area: computer-science
domain: software-architecture
section: ai-assisted-software-development
parent: "[[Software Architecture]]"
status: seed
related:
  - "[[OpenAI Codex]]"
  - "[[Model Context Protocol]]"
  - "[[Codex Skills]]"
  - "[[Codex Plugins]]"
tags: []
---

# AI-Assisted Software Development

## Краткое определение области

`AI-Assisted Software Development` — это обзорная ветка о программной инженерии, в которой значимая часть анализа, планирования, модификации кода и операционной координации делегируется агентным системам, умеющим работать с репозиторием, инструментами и внешними источниками контекста.

## Что входит в эту тему

- `[[OpenAI Codex]]`
- `[[AGENTS.md]]`
- `[[Codex Rules]]`
- `[[Codex Hooks]]`
- `[[Model Context Protocol]]`
- `[[Codex Skills]]`
- `[[Codex Plugins]]`
- `[[Codex Subagents]]`
- `[[AI-Assisted Programming]]`
- `[[AI-Assisted Project Management]]`
- `[[AI-Assisted Personal Effectiveness]]`

## Как устроена ветка

- `OpenAI Codex` задаёт общий продуктовый и исторический контекст.
- `AGENTS.md` и `Codex Rules` фиксируют инструкции и ограничения поведения агента.
- `Model Context Protocol` описывает стандарт подключения внешних инструментов и источников данных.
- `Codex Skills`, `Codex Plugins` и `Codex Hooks` образуют слой расширяемости и адаптации среды.
- `Codex Subagents` описывает механизм декомпозиции задач и параллельного агентного исполнения.
- Прикладные заметки показывают, как эти механизмы используются в программировании, управлении проектами и личной эффективности.

## Рекомендуемый маршрут чтения

1. Начать с `[[OpenAI Codex]]`.
2. Затем перейти к `[[AGENTS.md]]` и `[[Codex Rules]]`.
3. После этого прочитать `[[Model Context Protocol]]`.
4. Затем связать протокольный слой с `[[Codex Skills]]`, `[[Codex Plugins]]` и `[[Codex Hooks]]`.
5. Завершить чтением `[[Codex Subagents]]` и трёх прикладных заметок.

## Соседние overview-ветки

- Родительская рамка: `[[Software Architecture]]`
- Близкая инженерная перспектива: `[[Distributed Systems]]`

## Что стоит раскрыть дальше

- [ ] Добавить обзор по execution policy и sandboxing
- [ ] Добавить статью о tool-using agents
- [ ] Добавить заметку о handoffs и orchestration
- [ ] Проверить, нужен ли отдельный обзор по enterprise governance
