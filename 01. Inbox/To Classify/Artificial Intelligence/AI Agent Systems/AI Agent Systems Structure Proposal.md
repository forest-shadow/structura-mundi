# AI Agent Systems Structure Proposal

## Назначение

Этот файл фиксирует минимальную структуру ветки `AI Agent Systems`, в которой агентные системы рассматриваются как отдельный инфраструктурный слой внутри `Artificial Intelligence`.

## Рекомендуемая иерархия

```text
Artificial Intelligence
└── AI Agent Systems
    ├── Agent Protocols and Conventions
    │   ├── AGENTS.md
    │   └── Model Context Protocol
    └── OpenAI Codex
        ├── Codex Rules
        ├── Codex Hooks
        ├── Codex Plugins
        ├── Codex Skills
        └── Codex Subagents
```

## Почему структура именно такая

- Здесь полезно отделить общие agent patterns от частной реализации конкретного инструмента.
- `Agent Protocols and Conventions` собирает соглашения и протоколы, которые естественно переиспользуются между разными агентными платформами.
- `OpenAI Codex` выступает как tool-specific ветка со своей собственной конфигурацией и расширяемостью.

## Что не нужно создавать заранее

- отдельную overview-ветку под каждый небольшой конфигурационный механизм;
- отдельную ветку `MCP Tools`, если пока она дублирует `Model Context Protocol`;
- смешивать applied use cases с устройством агентных систем.

## Следующий шаг

1. Позже решить, нужен ли отдельный соседний обзор для других agent platforms.
2. Проверить, не перерастает ли ветка `Agent Protocols and Conventions` в самостоятельный более широкий кластер.
