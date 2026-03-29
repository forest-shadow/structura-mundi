# Codex Rules Structure Proposal

## Краткое определение

`Codex Rules` разумно держать как дочернюю `article`-заметку внутри `OpenAI Codex`.

## Рекомендуемая роль в иерархии

```text
OpenAI Codex
└── Codex Rules
```

## Почему так

- Это частный механизм policy и runtime governance внутри конкретного инструмента.
- Тема естественно живет рядом с hooks, plugins и skills.
- Для нее пока не нужен отдельный обзорный узел.

## Что не стоит создавать сейчас

- отдельный overview про permissions без соседних статей;
- дублировать общие agent governance conventions, которые должны жить вне tool-specific ветки.
