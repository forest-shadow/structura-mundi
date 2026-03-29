# Codex Plugins Structure Proposal

## Краткое определение

`Codex Plugins` разумно держать как дочернюю `article`-заметку внутри `OpenAI Codex`.

## Рекомендуемая роль в иерархии

```text
OpenAI Codex
└── Codex Plugins
```

## Почему так

- Это tool-specific упаковка расширений, а не общий агентный протокол.
- Тема полезно соседствует с hooks и skills.
- Подветка про plugin internals пока была бы слишком ранней.

## Что не стоит создавать сейчас

- отдельные дочерние статьи под manifest schema и marketplace details без накопленного материала;
- смешивать plugins с MCP как будто это один и тот же уровень абстракции.
