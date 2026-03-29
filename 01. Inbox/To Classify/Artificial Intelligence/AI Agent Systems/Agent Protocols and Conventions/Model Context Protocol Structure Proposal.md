# Model Context Protocol Structure Proposal

## Краткое определение

`Model Context Protocol` разумно держать как дочернюю `article`-заметку внутри `Agent Protocols and Conventions`.

## Рекомендуемая роль в иерархии

```text
Agent Protocols and Conventions
└── Model Context Protocol
```

## Почему так

- Это общий протокол интеграции, полезный шире одной платформы.
- Его удобно читать рядом с локальными instruction conventions, а не внутри tool-specific ветки.
- Тема уже достаточно самостоятельна для отдельной статьи, но пока не требует собственного поддерева.

## Что не стоит создавать сейчас

- отдельную ветку под transport details и JSON-RPC specifics без соседних статей;
- дублировать MCP внутри каждой vendor-specific ветки.
