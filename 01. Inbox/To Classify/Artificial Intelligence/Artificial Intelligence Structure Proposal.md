# Artificial Intelligence Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для доменной ветки `Artificial Intelligence` внутри `computer-science` по правилам `Principia Rerum`.

Словарная рамка для ветки теперь считается подтвержденной:

- `domain: artificial-intelligence`
- `section: ai-foundations`
- `section: applied-ai`
- `section: ai-agent-systems`
- `section: agent-protocols`
- `section: openai-codex`
- `section: ai-assisted-software-development`

## Рекомендуемая иерархия

```text
Computer Science
└── Artificial Intelligence
    ├── AI Foundations
    │   ├── Machine Learning
    │   ├── Generative AI
    │   └── Large Language Models
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

- `Artificial Intelligence` не стоит сводить только к прикладным use cases и агентным инструментам, поэтому понятийный слой вынесен в отдельную ветку `AI Foundations`.
- `AI Foundations` собирает базовые концепты поля, которые логически предшествуют прикладным сценариям и tool-specific конфигурациям.
- `Applied AI` сохраняет прикладную оптику: здесь ИИ выступает как рабочий инструмент в конкретных видах деятельности.
- `AI Agent Systems` сохраняет системную оптику: здесь ИИ рассматривается как агентная и инструментально оснащенная система.
- Внутри `AI Agent Systems` разумно отдельно держать общие протоколы и соглашения и tool-specific реализацию конкретной платформы.

## Что не нужно создавать заранее

- отдельный поддомен только под один vendor или один продукт, если рядом нет устойчивых соседних веток;
- отдельные тематические template-файлы под AI, потому что по `Principia Rerum` в vault должны оставаться только канонические `Article Template` и `Overview Template`;
- слишком глубокую академическую иерархию про все поддисциплины AI без накопленного корпуса заметок;
- смешивать foundations, applied и agent systems в одной плоской ленте статей.

## Созданные каркасы внутри ветки

- `Artificial Intelligence.md`
- `AI Foundations.md`
- `Machine Learning.md`
- `Generative AI.md`
- `Large Language Models.md`
- `Applied AI.md`
- `AI Agent Systems.md`

## Следующий шаг

1. Постепенно насыщать `AI Foundations` базовыми понятиями без преждевременного разрастания в отдельную учебную таксономию.
2. Добавлять новые прикладные ветки в `Applied AI` только по мере накопления реального корпуса заметок.
3. Позже решить, когда `Machine Learning` или `Generative AI` пора повышать из `article` в `overview`.
