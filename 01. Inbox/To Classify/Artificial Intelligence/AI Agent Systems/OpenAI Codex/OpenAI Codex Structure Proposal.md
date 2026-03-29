# OpenAI Codex Structure Proposal

## Назначение

Этот файл фиксирует минимальную tool-specific структуру для ветки `OpenAI Codex` внутри `AI Agent Systems`.

## Рекомендуемая иерархия

```text
AI Agent Systems
└── OpenAI Codex
    ├── Codex Rules
    ├── Codex Hooks
    ├── Codex Plugins
    ├── Codex Skills
    └── Codex Subagents
```

## Почему структура именно такая

- `OpenAI Codex` уже выступает не одной статьей, а устойчивым кластером про конкретную агентную платформу.
- `Codex Rules`, `Codex Hooks`, `Codex Plugins`, `Codex Skills` и `Codex Subagents` описывают разные механизмы одной и той же среды.
- Ветка не должна поглощать общие протоколы вроде `Model Context Protocol`, потому что они полезны шире одного инструмента.

## Что не нужно создавать заранее

- отдельный обзор под каждый мелкий runtime detail;
- отдельную ветку про enterprise governance до появления реального корпуса заметок;
- клон `OpenAI Codex` в прикладных use-case ветках.

## Следующий шаг

1. Позже решить, нужны ли отдельные статьи про Codex desktop, IDE integration и cloud tasks.
2. Проверить, не требуют ли `Codex Plugins` и `Codex Skills` собственных дочерних статей.
