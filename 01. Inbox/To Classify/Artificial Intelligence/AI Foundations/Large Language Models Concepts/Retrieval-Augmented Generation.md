---
aliases:
  - RAG
note_type: article
area: computer-science
domain: artificial-intelligence
section: ai-foundations
parent: "[[Large Language Models]]"
status: seed
related:
  - "[[Large Language Models]]"
  - "[[Prompt Engineering]]"
  - "[[Fine-Tuning]]"
tags: []
---

# Retrieval-Augmented Generation

## Краткое определение

`Retrieval-Augmented Generation` — каноническая статья про подход, в котором `[[Large Language Models]]` получают внешний контекст из retrieval-системы перед генерацией ответа.

## Основная идея или механизм

Объяснить, как система сначала находит релевантные фрагменты во внешнем корпусе, затем подмешивает их в контекст модели и только после этого запускает генерацию.

## Границы темы

- Входит: retrieval layer, document chunking, grounding, context injection, отличие parametric memory от external knowledge.
- Не входит: внутреннее устройство transformer и параметрическое дообучение как основной механизм адаптации.

## Связи с другими заметками

Родительская тема:

`[[Large Language Models]]`

Связанные заметки:

- `[[Prompt Engineering]]`
- `[[Fine-Tuning]]`
- `[[Transformer Architecture]]`

## Примеры, случаи или следствия

Показать, почему RAG особенно полезен для локальных баз знаний, быстро меняющихся фактов и задач, где нужна проверяемая опора на внешний корпус, а не только на параметры модели.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между retrieval grounding и model memory
- [ ] Добавить связь с embeddings и semantic search
- [ ] Проверить `related`
- [ ] Проверить `tags`
