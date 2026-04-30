---
aliases: []
note_type: article
area: computer-science
domain: artificial-intelligence
section: ai-foundations
parent: "[[Large Language Models]]"
status: seed
related:
  - "[[Large Language Models]]"
  - "[[Fine-Tuning]]"
  - "[[Prompt Engineering]]"
tags: []
---

# Transformer Architecture

## Краткое определение

`Transformer Architecture` — каноническая статья про архитектурную схему, на которой строится большинство современных `[[Large Language Models]]`.

## Основная идея или механизм

Объяснить, как transformer заменяет рекуррентную обработку механизмом attention и почему это позволяет эффективно моделировать длинный контекст и параллельно обучать LLM.

## Границы темы

- Входит: self-attention, positional encoding, encoder/decoder distinction, transformer blocks, scaling behavior в контексте LLM.
- Не входит: прикладная настройка модели, retrieval-слой и prompt-level управление поведением.

## Связи с другими заметками

Родительская тема:

`[[Large Language Models]]`

Связанные заметки:

- `[[Fine-Tuning]]`
- `[[Prompt Engineering]]`
- `[[Retrieval-Augmented Generation]]`

## Примеры, случаи или следствия

Показать, почему переход к transformer сделал возможными большие контекстные окна, instruction-following модели и современный скачок в генеративных LLM.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между encoder-only, decoder-only и encoder-decoder transformer
- [ ] Добавить связь с attention mechanism
- [ ] Проверить `related`
- [ ] Проверить `tags`
