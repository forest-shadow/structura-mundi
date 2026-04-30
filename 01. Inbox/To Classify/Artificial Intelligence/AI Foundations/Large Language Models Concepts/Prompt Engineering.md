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
  - "[[Retrieval-Augmented Generation]]"
tags: []
---

# Prompt Engineering

## Краткое определение

`Prompt Engineering` — каноническая статья про проектирование входного контекста для управления поведением `[[Large Language Models]]` без изменения их параметров.

## Основная идея или механизм

Объяснить, как инструкция, роль, примеры, формат входа и ограничения ответа влияют на распределение следующего токена и, следовательно, на наблюдаемое поведение модели.

## Границы темы

- Входит: system prompting, few-shot prompting, output constraints, prompt patterns, context design.
- Не входит: параметрическое дообучение модели и внешний retrieval как отдельный системный слой.

## Связи с другими заметками

Родительская тема:

`[[Large Language Models]]`

Связанные заметки:

- `[[Transformer Architecture]]`
- `[[Fine-Tuning]]`
- `[[Retrieval-Augmented Generation]]`

## Примеры, случаи или следствия

Показать, как одна и та же LLM может вести себя как краткий классификатор, аналитический ассистент или генератор структурированного JSON в зависимости от формы prompt.

## Что стоит раскрыть дальше

- [ ] Добавить различие между prompt engineering и instruction tuning
- [ ] Уточнить границу между prompt design и context engineering
- [ ] Проверить `related`
- [ ] Проверить `tags`
