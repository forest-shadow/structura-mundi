# Agent Protocols and Conventions Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию для ветки `Agent Protocols and Conventions`, где собираются общие агентные соглашения и протоколы.

## Рекомендуемая иерархия

```text
AI Agent Systems
└── Agent Protocols and Conventions
    ├── AGENTS.md
    └── Model Context Protocol
```

## Почему структура именно такая

- `AGENTS.md` и `Model Context Protocol` относятся к разным уровням, но оба описывают общий слой организации агентной работы.
- Ветка пока остается компактной и не требует дополнительного промежуточного overview.
- Tool-specific mechanisms нужно держать в соседней ветке `OpenAI Codex`, а не смешивать здесь.

## Что не нужно создавать заранее

- отдельную ветку под каждый instruction file format;
- отдельный overview про context sources, пока это только материал для связки с MCP;
- переносить сюда `Codex Skills` или `Codex Plugins`, потому что это уже частная реализация.

## Следующий шаг

1. Добавить соседние форматы instruction files, когда они появятся в корпусе.
2. Проверить, нужна ли отдельная заметка про prompt/governance conventions.
