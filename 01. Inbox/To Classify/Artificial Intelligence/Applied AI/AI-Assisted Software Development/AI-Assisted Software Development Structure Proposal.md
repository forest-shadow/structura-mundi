# AI-Assisted Software Development Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию для темы `AI-Assisted Software Development` как прикладного кластера внутри `Applied AI`, а не как корня всей AI-ветки.

## Рекомендуемая иерархия

```text
Applied AI
└── AI-Assisted Software Development
    └── AI-Assisted Programming
```

Соседние переиспользуемые ветки:

- `AI Agent Systems`
- `OpenAI Codex`

## Почему структура именно такая

- Тема описывает use case software engineering, а не общий каталог агентных механизмов.
- Общие протоколы, инструкции и tool-specific configuration лучше держать в соседней системной ветке и переиспользовать через `related`.
- На текущем этапе внутри software development уже явно выделяется `AI-Assisted Programming`, а другие подветки пока не требуют отдельных overview.

## Что не нужно создавать заранее

- переносить сюда `Model Context Protocol`, `AGENTS.md` или `Codex Skills`, потому что это соседний системный слой;
- заводить отдельный overview про sandboxing или orchestration до появления связанного корпуса заметок;
- смешивать project management и personal effectiveness с software engineering только потому, что они используют одни и те же агентные инструменты.

## Следующий шаг

1. Добавить статьи про AI-assisted code review, testing и refactoring по мере накопления материала.
2. Держать эту ветку прикладной, а не инфраструктурной.
