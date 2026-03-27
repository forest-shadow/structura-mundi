---
aliases:
  - Performance of Go Reflection
  - Performance and Limits of Go Reflection
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Go Reflection Mutation and Dynamic Calls]]"
  - "[[Go Reflection vs Generics vs Code Generation]]"
  - "[[Go Memory Management]]"
tags: []
---

# Go Reflection Performance and Limits

## Краткое определение

Статья о том, какие издержки и ограничения несет reflection в Go и почему их нужно оценивать как инженерные trade-offs, а не как универсальный запрет на runtime-метапрограммирование.

## Основная идея или механизм

Reflection добавляет runtime checks, часто приводит к дополнительным аллокациям, ухудшает часть compile-time guarantees и делает код менее прозрачным для оптимизаций и обычного чтения. Но корректная оценка ее стоимости требует контекста, а не лозунгов о том, что reflection всегда «на порядки медленнее».

## Границы темы

- В тему входят накладные расходы reflection, потеря части compile-time guarantees, корректное чтение benchmark и ограничения overly-generic решений.
- На границе находятся конкретные архитектурные альтернативы, которые лучше сопоставлять в отдельной статье.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[Go Reflection Mutation and Dynamic Calls]]`
- `[[Go Reflection vs Generics vs Code Generation]]`
- `[[Go Memory Management]]`

## Примеры, случаи или следствия

- Один и тот же reflection-подход может быть приемлем в редко исполняемом infrastructure-коде и проблемным в hot path.
- Некорректные benchmark-примеры часто сравнивают не сопоставимые сценарии и маскируют реальную цену abstraction choices.

## Что стоит раскрыть дальше

- [ ] Добавить источники типичных аллокаций и runtime checks
- [ ] Уточнить, как читать benchmark без ложных обобщений
- [ ] Проверить `related`
