# Artificial Intelligence Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для новой доменной ветки `Artificial Intelligence` внутри `computer-science` по правилам `Principia Rerum`.

На текущем этапе для этой ветки оправдано новое значение:

- `domain: artificial-intelligence` (предлагаемое новое значение)

## Рекомендуемая иерархия

```text
Computer Science
└── Artificial Intelligence
    ├── Applied AI
    │   ├── AI-Assisted Software Development
    │   │   └── AI-Assisted Programming
    │   ├── AI-Assisted Project Management
    │   └── AI-Assisted Personal Effectiveness
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

- Текущий материал уже шире, чем `AI-Assisted Software Development`, потому что включает не только software engineering, но и project management, personal effectiveness и общие agent mechanisms.
- Полезно развести прикладные сценарии (`Applied AI`) и инфраструктурный слой (`AI Agent Systems`).
- Внутри agent systems разумно отдельно держать общие протоколы и соглашения и tool-specific реализацию конкретной платформы.

## Что не нужно создавать заранее

- отдельный поддомен только под один инструмент, если кроме `OpenAI Codex` пока нет соседних платформ;
- слишком глубокую подветку про model families, пока основная масса заметок относится к applied и agentic use cases;
- отдельную обзорную ветку про `LLM Tools`, если её роль уже закрывается `AI Agent Systems`.

## Следующий шаг

1. Подтвердить `domain: artificial-intelligence` как рабочий домен внутри `computer-science`.
2. Наполнить `Applied AI` и `AI Agent Systems` как два устойчивых sub-overview.
3. Позже решить, нужна ли отдельная ветка про model-centric AI topics.
