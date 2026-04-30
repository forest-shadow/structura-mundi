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
  - "[[Prompt Engineering]]"
  - "[[Retrieval-Augmented Generation]]"
tags: []
---

# Fine-Tuning

## Краткое определение

`Fine-Tuning` — каноническая статья про дополнительную параметрическую адаптацию уже обученной модели в контексте `[[Large Language Models]]`.

## Основная идея или механизм

Объяснить, как дообучение на новом наборе данных меняет поведение модели и в каких случаях fine-tuning предпочтительнее, чем управление только через prompt или внешний retrieval.

## Границы темы

- Входит: supervised fine-tuning, domain adaptation, instruction tuning как частный случай, trade-offs по стоимости и устойчивости.
- Не входит: детальный разбор архитектуры transformer и внешний retrieval-пайплайн.

## Связи с другими заметками

Родительская тема:

`[[Large Language Models]]`

Связанные заметки:

- `[[Transformer Architecture]]`
- `[[Prompt Engineering]]`
- `[[Retrieval-Augmented Generation]]`

## Примеры, случаи или следствия

Показать, как fine-tuning может улучшать доменную лексику, формат ответов, стиль поведения и task-specific performance, но при этом добавляет стоимость обучения и риск деградации общих способностей.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между full fine-tuning и parameter-efficient adaptation
- [ ] Добавить связь с instruction tuning
- [ ] Проверить `related`
- [ ] Проверить `tags`
