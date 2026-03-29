# AGENTS Structure Proposal

## Краткое определение

`AGENTS.md` разумно держать как дочернюю `article`-заметку внутри `Agent Protocols and Conventions`.

## Рекомендуемая роль в иерархии

```text
Agent Protocols and Conventions
└── AGENTS.md
```

## Почему так

- Это устойчивый формат локальных агентных инструкций, а не частный runtime detail только одного инструмента.
- Тема естественно соседствует с протоколами контекста и tool integration.
- На текущем этапе отдельный sub-overview для instruction files был бы преждевременным.

## Что не стоит создавать сейчас

- отдельную ветку под каждый vendor-specific instruction file;
- отдельный overview про repository memory, если он пока полностью покрывается `AGENTS.md`.
